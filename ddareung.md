# 따릉이 스테이션별 예측 웹 개발 기여사항 및 트러블 해결

## [ppt](https://www.canva.com/design/DAGubIGg5RU/aEv3zbN8P67pXrYNil2OjA/view?utm_content=DAGubIGg5RU&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=ha4d5e86dd9)

### 기여 사항

#### 1. 공공데이터 수집 및 정제
> - 공공데이터 포털에 올라온 자료는 NaN값이 너무 많아 NaN값이 적은 API로 데이터 수집
> - 월별 CSV 저장 로직으로 수집 효율성을 개선하여 약 400만 건 이상의 데이터 확보

#### 2. 다양한 외부 변수 연동을 통한 예측 성능 향상
> - 기상청 날씨 데이터 연동: 온도, 습도, 불쾌지수 등 파생 변수 추가
> - 대여소 주변 정보 수집: 학교, 지하철 거리 정보를 기반으로 거리 기반 feature 생성

#### 3. 예측 모델링 및 성능 비교
> - 랜덤 포레스트 기반 회귀 모델을 사용해 시간별 대여량 예측 수행
> -	XGBoost와 비교하여 성능 및 해석력 분석
> -	MSE, MAE 등 지표를 기반으로 모델 선택 및 시각화 </br>
> -	예측값과 실제값 비교 시각화 (표1) </br>
> -	가중치를 주기 위한 시각화 (표2) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/bike%20image/real_pred.png?raw=true" width="400px" height="600px"/><br/>
      <span>표1</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/bike%20image/view%20weight.png?raw=true" width="400px" height="300px"/><br/>
      <span>표2</span>
    </td>
    </tr>
</table>


---

###  트러블 해결

#### 1. 대여소 정보와 이용 데이터 간 시계열 불일치 문제
> - 상황 : 대여소 정보와 이용 정보의 기준일자가 완전히 일치하지 않아 merge 시 데이터 누락 발생
> - 문제 : 단순 병합 시 이용 정보가 대량으로 빠지면서 예측 모델 성능이 하락됨
> - 해결 : 기준일자가 정확히 일치하는 대신, 이용 데이터의 기준일자가 대여소 정보의 유효기간 내에 포함되는 조건으로 merge를 수행하여 데이터 정확도와 누락률을 동시에 보완함

#### 2. 특정 시간대의 데이터 누락 문제
> - 상황 : 특정 대여소는 전체 시간 중 일부만 기록이 존재해 예측 정확도 저하 우려
> - 문제 : 전체 학습 데이터에 잡음으로 작용해 모델 전체 성능 저하
> - 해결 : 유사한 특성(예: 위치, 온도, 시간 등)을 가진 다른 대여소들을 선별하여, 해당 대여소의 결측 시간대 데이터를 유사 대여소들의 평균값으로 대체함.

#### 3. R² 계수 문제
> - 상황 : 24년도 데이터를 분할해서 train, valid, test를 한 후 값이 오류 없이 80% 이상이 나와서 25년 데이터로 예측을 진행
> - 문제 : 예측을 진행하니 R² 계수가 50 이하로 나옴
> - 해결 : 25년도 데이터를 살펴보니 타겟 데이터의 추세가 24년도와 달라서 해당 데이터에 가중치를 부여 함
