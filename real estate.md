# 부동산 아파트 전세 가격 예측 어플 기여사항 및 트러블 해결

## [ppt](https://www.canva.com/design/DAGtHNp4p1U/spIJD25MmBJgsc-5XXaw_Q/view?utm_content=DAGtHNp4p1U&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h5adea4ddf5)

### 기여 사항

#### 1. 데이터 전처리
> - 분석에 필요한 컬럼 추가
> - 나누어진 컬럼 통합
> - 데이터 그룹화 </br>

#### 2. 데이터 EDA
> - 상관 관계 heatmap 시각화 (표1)
> - 이상치 시각화 (표2) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/real%20estate%20image/outlier.png?raw=true" width="400px" height="400px"/><br/>
      <strong>표1</strong>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/real%20estate%20image/heatmap.png?raw=true" width="400px" height="400px"/><br/>
      <strong>표2</strong>
    </td>
  </tr>
</table>

#### 3. 데이터 시각화
> - 타겟과 상관관계가 있는 것들의 시각화(표 1,2,3) </br>
> - 예측값과 실제값 비교 시각화 (표4) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/real%20estate%20image/year&deposit.png?raw=true" width="400px" height="600px"/><br/>
      <span>표1</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/real%20estate%20image/area&deposit.png?raw=true" width="400px" height="300px"/><br/>
      <span>표2</span>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/real%20estate%20image/floor&deposit.png?raw=true" width="400px" height="300px"/><br/>
      <span>표3</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/real%20estate%20image/gongneung.png?raw=true" width="400px" height="300px"/><br/>
      <span>표4</span>
    </td>
  </tr>
</table>

#### 4. 최적의 모델과 하이퍼 파라미터 설정
> - 데이터의 이상치가 많기에 XGBregressor로 모델을 설정
> - 하이퍼 파라미터는 AutoML로 탐색 </br>

#### 5. 현재 매물 데이터 크롤링
> - python selenium을 이용한 부동산 114 크롤링 </br>
> - [시현영상](https://youtu.be/FQswd4jaI0g)


#### 6. 데이터 베이스 구축
> - NoSQL인 MongoDB로 데이터 베이스를 구축함 (표1) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/real%20estate%20image/mongodb.png?raw=true" width="400px" height="400px"/><br/>
      <strong>표1</strong>
    </td>
  </tr>
</table>

---

###  트러블 해결

#### 1. 하이퍼파라미터를 어떤 방식으로 찾아야하는지
> 1. GridSearchCV 와 AutoML중 어떤 방식을 사용할것인 가를 두고 의견충돌이 발생.
> 2. GridSearchCV는 하이퍼 파라미터의 범위를 정하고 찾는 방식이기에 정해진 시간안에 불가능하다고 판단 팀원들을 설득함.
> 3. 절충안으로 AutoML의 time_budget을 30분으로 정하기로 함.

