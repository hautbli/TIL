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

