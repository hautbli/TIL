장고실전
19.
백엔드와 프론트엔드

frontend ui layer

request/ response: data 전달(ex json)

backend business logic 

20.
restrul api  ->https://docs.microsoft.com/ko-kr/azure/architecture/best-practices/api-design

uri resource기반으로 (명사사용)

데이터 -> json형식

api 결과 -> 상태코드 로 반환
get method -> 200(정상) , 404 (리소스 찾을수없음)
post method-> 201 (새 리소스만드는 경우 )204(반환할 결과 없음)400(잘못된 데이터 요쳥)
put method -> 201, 200(기존리소스 업데이트) 204,409(충돌)


django rest framework
serialize -> form유사 , 데이터 검증 



장고 개발방식
mtv패턴
model : 데이터베이스에 저장되는 데이터
template 사용자에게 보여지는 부분
view 실질적으로프로그램 로직이 동작하여 템플릿에 전달

모델링의 순서
어떤 column이 필요한지?
어떤 field를 사용해야할지?

model relationship
many to many
many to one
one to one

primary key (기본키 ,pk)
테이블에 저장된 데이터를 유일하게 구분하는 키
기본키로 id가 디폴트로 지정됨

foreignkeky(외래키)
각 테이블을 연겨랗기 위해서 특정 테이블에서 다른 테이블의 참조되는 기본키

장고 필드 타입
추상 클래스 field클래스의 파생 클래스
charfield 작은 문자열 또는 큰 문자열을 위한 스트링 필드
textfield 큰 문자열 필드
integerfield 정수 필드
floatfield 실수 필드
booleanfield true/false
datetimefield 날짜와 시간을 가지는 필드
filefield 파일 업로드 필드
emailfield emailvalidator를 사용해서 깂이 유용한 email인지 체크
imagefield이미지 파일인지 유효성 체크 filefield의 파생 클래스
decimalfield소숫점을 갖는 필드
auto field 1부터 시작해서 1씩 증가해서 integerfield라고 볼 수 있다 pk 필드가 자동으로 추가됨
datefield datetime.date인스턴스로 표시되는 날짜의 필드 타입
auto_now_add 데이터가 처음 생성되어 저장
auto_now 데이터 수정할 때


user model확장
proxy model 사용
하나의 모델 정의 후 user모델과 one to one 관계 형성
abstract base user ->  아예 처음부터
abstract user ->  내장유저모델을 사용하면서 부분적으로 사용

