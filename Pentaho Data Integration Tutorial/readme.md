# Pentaho 튜토리얼
다음은 Hitachi에서 제공하는 Pentaho 튜토리얼을 틀로 하고 개인적으로 조사한 Pentaho ETL 튜토리얼을 문서화한 기록이다.
크게 6단계로 되어 있고, pentaho 에서 제공하는 툴인 PDI(Pentaho Data Integration)를 이용해서 data transformation과 job을 만드는 과정에 대해서 다룰 것이다.

### PDI가 만드는 파일 타입 2가지

## Transformation
> ETL에서 데이터의 흐름에 대한 작업을 담당하고 있다. 예를 들어, source로부터 데이터를 읽는다거나, 데이터를 transform 하여 target location으로 파일을 보내는 역할을 하기도 한다. 
## job
> job은 ETL에서 이루어지는 모든 일에 대해서 협동이 가능하게 도와준다. 흐름을 정의하거나, 다른 Transformation의 의존성에 대한 정의를 하거나, 파일 전송을 위해 파일 전송이 준비되어 있는지 유효성 검사를 하거나 데이터베이스에 테이블이 존재하는지 확인하는 기능을 하기도 한다. 

곧, 진행하고자 할 튜토리얼은 PDI를 이용해서 transformation을 만드는 것 부터, sales data에 대한 파일을 전송해서 메일 리스트를 만드는 것까지 한다. 데이터를 살펴보면 몇몇 고객의 zip code(주소)가 누락 된 것을 확인 할 수 있다. PDI의 preview를 보게 된다면, cleanse를 하거나 format을 만들거나 표준화, 샘플 데이터를 분류하는 것까지 가능하다는 것을 확인할 수 있을 것이다. 


### 튜토리얼 6단계

1. <b>flat file(csv 파일)을 가져와 rdb에 적재하는 과정</b>

2. <b>주소가 없는 records를 필터</b>

3. <b>Lookup과 Formatting을 사용해서 누락된 데이터를 해결</b>

4. <b>Mapping과 Ranges를 사용해 데이터를 정재</b>

5. <b> execution engine에서 transformation을 실행</b>

6. <b>job을 진두지휘</b>

