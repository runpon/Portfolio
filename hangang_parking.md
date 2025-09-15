# 한강공원 주차수요 예측 및 한강 공원내 이용자를 위한 서비스 APP & WEB 기여사항 및 트러블 해결

## [ppt](https://www.canva.com/design/DAGwye9VSA4/epAIhlsB6tV53YZGv0qh4g/view?utm_content=DAGwye9VSA4&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h07ce3301a9)

### 기여 사항

#### 1. 데이터 베이스
> - 요구 사항을 기반으로 1차적으로 ERR 설계  (표1)
> - 설계한 ERR를 기반으로 MongoDB로 변환 (표2)

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/hangangpark%20image/MongoDB.png?raw=true" width="400px" height="400px"/><br/>
      <strong>표1</strong>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/hangangpark%20image/EER.png?raw=true" width="400px" height="500px"/><br/>
      <strong>표2</strong>
    </td>
  </tr>
</table>

#### 2. 분석 및 머신러닝
> - 통계적 분석 (표1)
> - 버스 승하차객 머신러닝 (표 2 - 표 3) </br>
> - 주차장 이용량 머신러닝 (표 4 - 표 5) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/hangangpark%20image/T-Test.png?raw=true" width="400px" height="600px"/><br/>
      <span>표1</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/hangangpark%20image/real_pred1.png?raw=true" width="400px" height="300px"/><br/>
      <span>표2</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/hangangpark%20image/real_pred2.png?raw=true" width="400px" height="300px"/><br/>
      <span>표3</span>
    </td>
    </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/hangangpark%20image/Shap%20Value.png?raw=true" width="400px" height="300px"/><br/>
      <span>표4</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/hangangpark%20image/FeatureImportance.png?raw=true" width="400px" height="300px"/><br/>
      <span>표5</span>
    </td>
  </tr>
</table>

---

#### 1. 시간대 불균형(야간/심야)
> - 상황: 심야 구간 데이터로 인한 데이터 불균형이 나타남(주차장은 12시까지 운영).
> -	문제: 해당 구간의 오차 증가.
> -	해결: 시간대 별 가중치를 부여하여 데이터를 삭제하지 않고 제한적으로 적용되게 함
> - 효과: 심야 MAE 평균 –9% 개선.
