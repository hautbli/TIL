form
출처:https://developer.mozilla.org/ko/docs/Learn/Server-side/Django/Forms

[개요]
1. 웹 페이지상에서 한 개 이상의 필드, 위젯의 묶음
2. 사용자로부터 정보 수집 -> 서버 제출
3. csrf(cross-site request forgery protection)교차 사이트 요청 위조 방지
  와 함께 post 요청으로 데이타 전송 지원 -> 비교적 안전

* html form 이란?
서버의 역할
1.초기 form상태 표시(empty or initial values)
2.데이타의 유효성 검증
 - validate x -> error message
 - validate -> 적절한 동작(검색결과 반환/파일 업로드/ 데이터 저장 등)

* django form 처리 과정
요약: 뷰 (요청받음) -> context를 전달받은 템플릿으로 html page생성후 반환

1. unbound상태
-user가 처음으로 form을 request할 때 기본 form을 보여줌
-> 비어진 field 또는 initial field (initial 있어도 user가 입력한 값과 연관x -> unbound)

2.collect data and 결합 from submit request
- data를 form에 결합(binding) 
-> 유효성 위반한 경우 에러 메세지가 form을 재표시할 준비가 됨을 의미

3. 데이타를 다음어서 유효성 검증
- 사용자 입력을 sanitisation(정화)하고 python에서 사용하는 타입의  데이타로 변환

4. 유효하지 않은 데이터 -> 에러메세지 
5. 유효한 데이터 -> 요청된 데이터 수행
6. 모든 작업 완료 -> 사용자를 새로운 페이지로 보냄

* form 작성 - ex 대여기간 갱신 페이지 
1. form 선언
- model과 유사
from django import forms
    
class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")

2. 유효성 체크 
- self.cleaned_data['renewal_date']를 이용하여 데이타를 획득하고
 이 데이터의 수정여부에 상관 없이 데이터를 반환
 -> 유효성 검사도구를 이용해 입력값을 다듬고(cleaned) 저어화하며 표준 형식으로 변환
 - 입력값이 범위를 벗어날 경우 validation error 발생 erro message 지정
 


