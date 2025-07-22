# 온담 어플 기여사항 및 트러블 해결

## [ppt](https://www.canva.com/design/DAGppeL19Ek/X5NdAqmEmtaO4Xup4amGcw/view?utm_content=DAGppeL19Ek&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h9dd7a23317)

### 기여 사항

#### 1. 데이터 베이스 모델링
> - 요구 사항들을 ERD로 1차적으로 설계 (표1)
> - 1차 설계한 것들을 EER로 2차 설계 (표2)

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_erd.png?raw=true" width="400px" height="400px"/><br/>
      <strong>표1</strong>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_eer.png?raw=true" width="400px" height="500px"/><br/>
      <strong>표2</strong>
    </td>
  </tr>
</table>

#### 2. 본사 데이터 시각화
> - 본사 대쉬보드 제작 (표1)
> - 상세 정보 시각화 (표 2,3,4,5,6) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_hq_main.png?raw=true" width="400px" height="600px"/><br/>
      <span>표1</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_hq_graph1.png?raw=true" width="400px" height="300px"/><br/>
      <span>표2</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_hq_graph2.png?raw=true" width="400px" height="300px"/><br/>
      <span>표3</span>
    </td>
    </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_hq_graph3.png?raw=true" width="400px" height="300px"/><br/>
      <span>표4</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_hq_graph4.png?raw=true" width="400px" height="300px"/><br/>
      <span>표5</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_hq_graph5.png?raw=true" width="400px" height="300px"/><br/>
      <span>표6</span>
    </td>
  </tr>
</table>

#### 3. 대리점 데이터 시각화
> - 본사 대쉬보드 제작 (표1)
> - 상세 정보 시각화 (표 2,3,4,5,6) </br>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_store_status.png?raw=true" width="400px" height="600px"/><br/>
      <span>표1</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_store_detail1.png?raw=true" width="400px" height="300px"/><br/>
      <span>표2</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_store_detail2.png?raw=true" width="400px" height="300px"/><br/>
      <span>표3</span>
    </td>
    </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_store_analysis1.png?raw=true" width="400px" height="300px"/><br/>
      <span>표4</span>
    </td>
    <td align="center">
      <img src="https://github.com/runpon/Portfolio/blob/main/ondam%20image/ondam_store_analysis2.png?raw=true" width="400px" height="300px"/><br/>
      <span>표5</span>
    </td>
  </tr>
</table>

---

###  트러블 해결

#### 1. 중간에 데이터 베이스에 relation이나 entity를 추가하자
> 1. 앱을 만들던 중 테이블이 움직이는 기능이 필요하다고 팀원이 주장
> 2. 지금 데이터 베이스를 고치려면 처음부터 다시 설계 후 만들어야 하기에 시간적으로 힘들다고 설득
> 3. 절충안으로 새로운 relation을 만들어서 기존 데이터 베이스를 수정하는 것으로 마무리
