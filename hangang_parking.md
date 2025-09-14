# 한강공원 주차수요 예측 및 한강 공원내 이용자를 위한 서비스 APP & WEB 기여사항 및 트러블 해결

## [ppt](https://www.canva.com/design/DAGwye9VSA4/epAIhlsB6tV53YZGv0qh4g/view?utm_content=DAGwye9VSA4&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h07ce3301a9)

### 기여 사항

#### 1. 데이터 베이스
> - 요구 사항을 기반으로 1차적으로 ERD 설계  (표1)
> - 1차 ERD를 기반으로 NoSQL 설계 (표2)

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_erd.png?raw=true" width="400px" height="400px"/><br/>
      <strong>표1</strong>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_eer.png?raw=true" width="400px" height="500px"/><br/>
      <strong>표2</strong>
    </td>
  </tr>
</table>

#### 2. 분석 및 머신러닝
> - 통계적 분석 (표1)
> - 버스 승하차객 머신러닝 (표 2 - 표 6) </br>
> - 주차장 이용량 머신러닝 (표 2 - 표 6) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_hq_main.png?raw=true" width="400px" height="600px"/><br/>
      <span>표1</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_hq_graph1.png?raw=true" width="400px" height="300px"/><br/>
      <span>표2</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_hq_graph2.png?raw=true" width="400px" height="300px"/><br/>
      <span>표3</span>
    </td>
    </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_hq_graph3.png?raw=true" width="400px" height="300px"/><br/>
      <span>표4</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_hq_graph4.png?raw=true" width="400px" height="300px"/><br/>
      <span>표5</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_hq_graph5.png?raw=true" width="400px" height="300px"/><br/>
      <span>표6</span>
    </td>
  </tr>
</table>

---

###  트러블 해결

#### 1. 개발 도중 추가된 기능 요구로 인한 DB 수정 이슈
> - 상황 : 앱 개발 중 특정 UI에서 테이블이 동적으로 움직이는 기능이 필요하다는 팀원의 요구가 발생
> - 문제 : 이 기능을 구현하기 위해서는 기존 데이터베이스를 처음부터 다시 설계해야 했고, 이는 프로젝트 일정에 큰 영향을 줄 수 있음
> - 해결 : 팀원들과 논의 후 기존 데이터베이스 구조는 유지하고, 새로운 관계(Relation)를 추가하는 방식으로 기능을 반영하여 문제를 해결
