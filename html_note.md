# HTML 기초

## HTML(Hyper Text Markup Language)
  *웹페이지를 제작할 때 기본 구조를 만드는 언어*
	이 영역이 무슨 역할을 하는지 인지시킴
	태그와 상관없이 css로 그럴싸한 페이지의 모양새를 만들 수 있음.
	하지만 구조가 부실하며 접근성이 떨어짐.
  *디자인적 요소가 포함되지 않음*
	글꼴, 크기, 정렬, 색깔 > css


## 용어 정리
  *태그*
    명령어의 형태가 <>로 되어 있는 것들

  *요소 - element*
	태그의 시작(열린 태그 <>)과 끝(닫힌 태그 </>) 한 쌍을 의미.

  *마크업*
	요소들을 이용하여 웹 문서를 작성하는 것.

  *속성 - attributes*
	태그의 요소에 지정하는 것들
	열린 태그에만 쓰며 띄어쓰기로 구분한다.
    	ex) <a href="" target="_blank">에서 
	        href, target이 속성


## 태그와 요소
  태그는 각자의 구조적 의미를 가진다.
  요소는 열린 태그 <>로 시작해 닫힌 태그 </>로 끝나며
   이 구조는 태그의 범위를 만들어준다.

  *빈 태그* : 닫힌 태그 없이 열린 태그 단독으로 쓰인다.
		    속성 부여 불가
	<br>	텍스트 안에 줄바꿈(*Carriage Return)을 생성
	<hr>	가로방향의 Division Line를 생성
	<img>	이미지를 생성
	<input>	사용자의 데이터를 받을 수 있는 대화형 컨트롤을 생성함
	<link>	현재 문서와 외부 리소스의 관계를 명시
	<meta>	<base>, <link>, <script>, <style>, <title>과 같은 다른 메타 관련 요소로 나타낼 수 없는 메타데이터를 나타냄
 

## 속성(attributes) = "값(value)"
  *속성* 
   태그의 기능을 확장해서 사용할 수 있게 한다.
   속성은 열린 태그 안에 작성하며 띄어쓰기로 구분한다.
       <TAG 속성="값"></TAG>
       <a href="#" class="naver-link">네이버</a>

  *논리 속성* : 별도의 값 없이 사용
   			   쓰면 적용, 안 쓰면 미적용
			   select, disabled 등이 있다

  *개별 속성* : 특정 태그에 특정하게 쓸 수 있는 속성
       ex) a-href / img-src

  *전역 속성* : 태그 상관없이 쓸 수 있는 속성
	- class : 요소의 별칭을 지정
	    	  보통 그룹화할 때 사용
		      한 요소에 '여러' class 지정 가능
    - id : 요소에 고유의 식별자를 정의
	       보통 특정 요소를 '단독'으로 지칭할 때 씀

	- style : css를 인라인으로 적용시킬 때 씀
    - title : 요소에 마우스 포커스했을 때 설명 지정
	          <abbr>의 속성이기도 함
    - data-* : JavaScript할 때 씀


## 부모요소 / 자식요소 - 형제요소
  태그는 *중첩* 기능을 통해 부모 자식요소의 단계적 구조 만들 수 있다.
<nav>			       부모
  <h1>대전 맛집></h1>   nav 자식, ul 형제
  <ul>                 nav 자식, h1 형제
    <li>성심당1</li>    nav 후손, ul 자식, li 형제
    <li>성심당2</li>
    <li>성심당3</li>
  </ul>
</nav>

## HTML 기본 구조
<!DOCTYPE html>
   현재 문서는 HTML표준 규칙을 따른다는 의미.
   다양한 브라우저에서 마크업이 동일하게 화면에 표현될 수 있다.

<html> 요소
   모든 html문서는 항상 이 요소 안에 마크업해야 한다.
   기본적으로 <head>와 <body> 요소로 구성되어 있다.

 	<head> 요소
	  문서의 속성이나 설정을 지정한다.
	   <meta> 문서의 설명, 키워드, 저자
	   <title> 문서의 제목
	   <link> 일반적으로 '외부 CSS파일' 연결 시 사용
	   <script> 주로 '자바스크립트'를 선언 시 사용
	   <style> 문서 내에서 '직접 스타일(CSS)'을 정의
	</head>

 	<body> 요소
	  실제로 사용자에 보여질 화면을 마크업
	</body>
</html>

------------------------------------------------------------

# 태그

## 블록 요소와 인라인 요소
 1. 블록 요소
   사용 가능한 최대 가로 너비를 점유
     > 마크업 시 자동으로 줄바꿈이 일어남
     > 가로, 세로 크기 지정 가능
   또 다른 블록 요소와 인라인 요소 중첩 가능
   거의 대부분의 태그가 블록 요소의 성질을 갖고 있다.

 2. 인라인 요소
   필요한 만큼의 너비를 사용
	 > 마크업 시 자동 줄바꿈 없음 (한 줄에 출력)
	 > 가로 세로 크기 지정 불가
   텍스트와 인라인 요소 중첩 가능, 블록 요소는 중첩 불가
	<a> <abbr> <br/> <button> <em> <i> <img> <input>  <label>
	<script> <select> <span> <strong> 등등


## 콘탠츠 구분 태그

 1. <h1> ~ <h6>
   문서의 제목이나 목차를 지정할 때 사용한다.
   각각의 <article>이나 <section>을 식별할 때 자식요소로 사용 가능.
   구조를 탄탄히 해 접근성을 높일 수 있다.
   건너뛰지 말고 <h1>부터 순서 맞춰 쓰기
    <h1>
	 가장 높은 순위의 태그.
	 로고, 문서의 대제목 등 해당 페이지의 목적을 설명하는 데 쓰임
	 단 한 번만 사용하는 걸 권장한다.


 2. <header>
   로고, 검색 폼, 메뉴 네비게이션 등을 포함하는 요소
   웹페이지의 소개, 메뉴 등 탐색에 도움을 주는 내용을 담는다.

 3. <footer>
   일반적으로 작성자, 저작권 정보, 관련 문서 등의 내용을 담는다.

 4. <article>
   사이트 안에서 독립적으로 구분해서 배포하거나 재사용할 수 있는 영역을 나타낸다.
   게시판, 블로그 글, 매거진, 뉴스, 기사 등에 사용

 5. <section>
   문서의 일반적인 영역을 나타낼 때 사용.
   스타일링을 위한 컨테이너보다(div 추천) 구획을 논리적으로 요약할 때 사용하는 것을 권장한다.
   요소의 콘텐츠를 따로 구분할 필요가 있다면 article을 추천

 6. <aside>
   주로 사이드바, 광고 배너를 마크업할 때 사용

 7. <nav>
   메뉴, 목차, 색인 등 다른 페이지로의 링크를 보여주는 영역

 8. <div>
   CSS로 스타일링하거나 아무 의미가 없는 영역을 구성할 때 사용
   내용에 적합한 다른 태그가 있는지 고려해본 뒤 사용할 것

 9. <ol> <ul> <li>
   ol(orderd list) : 순서가 구분될 필요가 있는 목록
   ul(unorderd list) : 순서가 필요 없는 목록
   li(list item) : ol과 ul의 자식 태그로 항목을 나열할 때 쓰임
			     단독 사용이 불가하며 다른 태그 중첩은 가능.

 10. <p> <hr>
   p(paragraph) : 하나의 문단을 설정할 때 사용
				인라인 태그만 중첩 가능
   hr(horizontal rule) : 문단들을 분리할 때 사용
					  빈 태그(열린 태그만 단독 사용)

## 인라인 텍스트 태그

1. <a>
  href 속성을 통해 다른 URL로 연결할 수 있는 하이퍼링크 생성
  내용으로는 링크의 설명이 들어감

2. <abbr>
  준말, 머리글자 나타냄.
  선택속성 title을 사용하면 마우스 포인팅으로 설명 제공 가능

3. <span> <b> <mark> <em> <strong>
  span: 인라인 텍스트 콘텐츠를 위한 공용 컨테이너
       본질적으로 아무 의미가 없으며 블록요소의 div와 유사한 용도

  b: 독자의 주의를 끌기 위한 용도
    요약 키워드, 리퓨 제품명 등 특별히 중요하지는 않지만 굵게 처리하고 싶을 때
  
  mark: 사용자의 관심을 하이라이팅할 때

  em: 단순한 의미 강조

  strong: 아주 높은 중요도를 가진 곳을 표시

4. <br>
  줄을 바꿀 때 사용.
  빈 태그(닫는 태그 없이 열린 태그 단독 사용)


## 멀티미디어 태그 
1. <img>
  이미지를 삽입하는 태그
  src: 이미지의 URL(필수)
  alt: 이미지의 대체 텍스트(필수)
  width, height: 이미지의 가로, 세로 너비
  
2. <audio> <video>
 소리, 영상 콘텐츠를 삽입하는 태그

 src: 콘텐츠 URL
 autoplay: 준비되면 바로 재생(논리값)
 controls: 제어 메뉴를 표시(논리값)
 loop: 재생이 끝나면 처음부터 다시 재생(논리값)
 muted: 음소거(논리값)
 poster: 동영상 썸네일 이미지 URL
 width, height: 동영상의 가로, 세로 너비

 *autoplay, loop> 크롬에서는 지원하지 않음

3. <iframe>
 다른 HTML 페이지를 현재 페이지에 삽입(멀티미디어 링크 가능)

 src: 포함할 문서의 URL(필수)
 name: 프레임의 이름
 width, height: 프레임의의 가로, 세로 너비
 allowfullscreen: 전체화면 모드(논리값)
 frameborder: 프레임 테두리(0, 1)


## 표 콘텐츠 태그
<table>
표를 만들기 위해 사용하는 태그.
tr을 자식요소로, th와 td를 후손으로 삼는다.
  <tbody> 보이지 않아도 자동으로 삽입되어 있다
    <tr> ↓ table row, 행(세로 몇 줄인지)
      <th> → table header, 첫 줄, 열의 제목(가로 몇 칸인지)
    </tr>
    <tr>
      <td> → table data, 각 열의 데이터(가로 몇 칸인지) 
    </tr>
  </tbody>
</table>

  abbr: 열에 대한 간단한 설명
  headers: 관련된 하나 이상의 다른 머리글 칸 id 속성 값

  colspan: 병합하려는 열의 수(값만큼 가로칸을 점유한다)
  rowspan: 병합하려는 행의 수(값만큼 세로칸을 점유한다)


## 입력양식(form)
1. <form>
 웹 서버에 정보를 제출하기 위한 양식을 정의하는 요소

 *속성*
 action : 입력 데이터를 어디로 전송할지 쓴다 
          전송한 정보를 처리할 (URL)을 쓴다

 name : 양식의 고유한 이름

 method : 서버로 전송한 HTTP 방식 (get / post)
    get: 입력값이 주소창에 남는다(링크를 복붙 가능)
    post: 입력값이 주소창에 안 남는다(보안사항)
         입력 안 하면 get 기본
 
 autocomplete : 사용자가 이전에 입력한 값으로 자동완성 기능을 사용할 것인지 여부(on / off)
 
 novalidate : 서버로 전송 시 양식 데이터의 유효성을 검사하지 않도록 지정(논리값)
              자동 검증하지 않음
              html5에서는 별도 값을 입력하지 않아도 된다.
 
 taget : 서버로 전송 후 응답받을 방식을 지정(_self / _blank)

  ip와 url 
    https://github.com/sokoving/git_study
                ip    /  url

2. <input>
 사용자에게 입력받을 데이터 양식을 지정
 빈 태그

 *속성*
 type: 입력받을 데이터의 종류(하단 별도 정리)
 value: 양식의 초기값
 name: 양식의 이름

 placegolder: 사용자가 입력할 값의 힌트(예시)
 checked: 양식이 선택된 상태로 시작(논리값)
 disabled: 양식을 비활성화
 readonly: 수정 불가한 읽기 전용(논리값)

 *type*
 text: 일반 텍스트
 password: 비밀번호(입력값을 구별할 수 없게 처리됨)
 email: 이메일
 search: 검색
 number: 숫자
 file 파일

 checkbox: 체크박스(복수 선택)
 radio: 라디오(단수 선택)
 button: 일반 버튼 (<button>보다 좀 더 단순)
 
 range: 범위 컨트롤 (min, max, step, value 속성 사용)

 hidden: 몰래 서버로 전송할 내용(value 속성으로 값을 지정)


3. <label>
 입력 양식(input)의 제목 역할
 label로 영역을 묶어 정확한 input 칸을 클릭 안 해도 되게 함

 for 속성을 사용해 입력양식과 연결
   >> <input id="aaa"> <laber for="aaa">

4. <button>
    <button type="button">그냥 버튼</button> 개발자 커스텀 기능을 넣을 수 있다
    <button type="reset">초기화 버튼</button> form내부 양식 모두 제거(초기화 버튼)
    <button type="submit">전송 버튼</button> form내용을 서버로 전송 (추가 질문으로 쿠션을 넣자)

5. <textarea cols="20" rows="5"></textarea>
  여러 줄의 일반 텍스트를 입력할 수 있다

  cols (column, 열, 기둥, 세로)
    cols="20" > 알파벳 20개가 한 줄
  rows (행, 가로)
   rows="5" > 기본값 5줄, 이상은 스크롤

6. <select>
    <optgroup label="Coffee">   label: 커피와 주스를 각각 라벨을 붙여서 그룹화함
      <option>Americano</option>
      <option selected>Caffe Latte</option>         selected: 초기 선택
      <option disabled>Capuccino(Sold out)</option> disabled: 선택 불가
    </optgroup>

    <optgroup label="Juice">
      <option>Orange Juice</option>
      <option>Lime Juice</option>
    </optgroup>
  </select>

----------------------------------------------------------
# 전역 속성
 - HTML 요소에서 공통 사용 가능한 속성
 1. class
   요소의 별칭 지정, 공백을 통해 여러 클래스 지정
   CSS나 JS에서 요소를 제어할 때 사용
 2. id
   고유한 식별자 정의

 * class는 여러 요소에 중복으로 설정 가능하지만
   id는 단 하나의 요소에만 사용

 3. style
   요소에 직접 스타일을 지정할 때 사용(인라인 스타일)

 4. title
   요소에 마우스를 포커스했을 때 설명을 지정

 5. data-*
  사용자 정의 데이터 속성
   JS에서 이용할 수 있는 데이터를 저장해두는 용도

# 상대경로: 나를 기준으로 찾아감
		 ./ : 현재 폴더에서 진입함(생략 가능)
		 ../ : 상위 폴더로 나가서 진입함
# 절대경로: 고유 주소로 찾아감(풀경로)
		  파일 주소가 유동적일 때 사용
		E:\git_study
		http://~~

## 특수문자 기호
&nbsp; : 스페이스 공백
&lt; : <
&gt; : >
&amp; : &

추가 내용 : https://www.freeformatter.com/html-entities.html