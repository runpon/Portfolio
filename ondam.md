# 온담 어플 기여사항 및 트러블 해결

## [ppt](https://www.canva.com/design/DAGppeL19Ek/X5NdAqmEmtaO4Xup4amGcw/view?utm_content=DAGppeL19Ek&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h9dd7a23317)

### 기여 사항

#### 1. 데이터 베이스 모델링
> - 요구 사항을 기반으로 1차적으로 ERD 설계  (표1)
> - 1차 ERD를 기반으로 EER 모델로 확장하여 2차 설계 (표2)

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

#### 2. 본사 데이터 시각화
> - 본사용 대쉬보드 제작 (표1)
> - 상세 지표 시각화 (표 2 - 표 6) </br>
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

#### 3. 대리점 데이터 시각화
> - 대리점용 대쉬보드 제작 (표1)
> - 상세 지표 시각화 (표 2 - 표 6) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_store_status.png?raw=true" width="400px" height="600px"/><br/>
      <span>표1</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_store_detail1.png?raw=true" width="400px" height="300px"/><br/>
      <span>표2</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_store_detail2.png?raw=true" width="400px" height="300px"/><br/>
      <span>표3</span>
    </td>
    </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_store_analysis1.png?raw=true" width="400px" height="300px"/><br/>
      <span>표4</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/data/ondam%20image/ondam_store_analysis2.png?raw=true" width="400px" height="300px"/><br/>
      <span>표5</span>
    </td>
  </tr>
</table>

---

###  트러블 해결

#### 1. 개발 도중 추가된 기능 요구로 인한 DB 수정 이슈
> - 상황 : 앱 개발 중 특정 UI에서 테이블이 동적으로 움직이는 기능이 필요하다는 팀원의 요구가 발생
> - 문제 : 이 기능을 구현하기 위해서는 기존 데이터베이스를 처음부터 다시 설계해야 했고, 이는 프로젝트 일정에 큰 영향을 줄 수 있음
> - 해결 : 팀원들과 논의 후 기존 데이터베이스 구조는 유지하고, 새로운 관계(Relation)를 추가하는 방식으로 기능을 반영하여 문제를 해결
