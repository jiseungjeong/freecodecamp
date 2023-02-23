# Full Stack Web Dev for Beginners
## Introduction
> Reference: 
> - freecodecamp "https://www.youtube.com/watch?v=nu_pCVPKzTk"
> - 조코딩 웹프로그래밍 "https://www.youtube.com/watch?v=ZeD8yNMYe-o&list=PLU9-uwewPMe2-R9-taf4oIjwrEZDgE-q2"
> - mdn docs: https://developer.mozilla.org/ko/

추가적으로 codecademy의 html 배우기 시리즈 "https://www.codecademy.com/courses/learn-html/" 를 통해 html에 대해 공부하는 것을 추천함. 아래는 freecodecamp 영상의 내용을 정리한 것임.
- Page
    - HTML : **Structure**
    - CSS: **Styling**
    - JS: **Functionality**

일반적으로 위와 같은 구조로 웹사이트가 구성된다.
- 집
    - 침대 2개: **구조**
    - 벽돌: **스타일링**
    - 먹기: **기능성**

위와 같이 예시를 들수도 있다.

유저가 보고 상호작용하는 부분 부분을 주로 **`프론트엔드`** 라고 표현하며, **`백엔드`** 는 서버 및 프론트엔드에 전원을 공급하는 역할을 한다. 데이터 베이스, 어플리케이션 로직, API를 제공한다. 여러 동적 콘텐츠를 위해 백엔드가 필요한 것이다.

## Learn HTML
> https://replit.com/ 레플잇을 사용하여 강의를 진행한다.

HTML 코드 작성이 즉시 어떻게 반영되는지 한 눈에 파악할 수 있기에 레플잇을 사용하여 HTML을 직접 만져볼 것을 추천한다.

~~~
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>replit</title>
  <link href="style.css" rel="stylesheet" type="text/css" />
</head>

<body>
  Hello world
  <script src="script.js"></script>

  <!--
  This script places a badge on your repl's full-browser view back to your repl's cover
  page. Try various colors for the theme: dark, light, red, orange, yellow, lime, green,
  teal, blue, blurple, magenta, pink!
  -->
  <script src="https://replit.com/public/js/replit-badge-v2.js" theme="dark" position="bottom-right"></script>
</body>

</html>
~~~

아래와 같은 맨 처음 html 코드가 주어진다.
그 외에도 CSS, JS 코드도 주어지지만 지금 당장 고려할 필요는 없다.

~~~
<!DOCTYPE html>
<html>

<head>
  <title>replit</title>

<body>
  Hello world
</body>

</html>
~~~
간략하게 HTML만 보자면 위 구조다.
### 여러 태그들
- `<h1 style="color:blue; background-color:red"> </h1>` , h2, h3 ... h6, 이렇게 스타일을 CSS 파일을 만들지 않고도 직접 지정할 수 있다.
    > <h1 style="color:blue; background-color:red">이게 h1이다.</h1>
- `<p title="test"></p>`: title 속성은 마우스 갖다댔을 때 나오는 작은 텍스트다.
    > <p title="test">이건 문단을 나타낸다.</p>
기본적으로 `<tag> 내용 </tag>` 와 같은 구조이다.
- `<!DOCTYPE html>`: 문서의 타입을 나타내며 일반적으로 HTML 코드 맨 윗단에 쓰인다.
- `<html></html>`: html 콘텐츠가 담기는 태그
- `<body></body>`: html 태그안에 들어감

- `<a href="https://google.com" target="_blank" ></a>`: 링크를 담을 수 있는 태그 (앵커, 닻을 의미), 타겟 블랭크는 새탭에서 열기 의미, 아이디를 이용하여 기존 탭에서 그 아이디 portion part로 이동 가능 ex) `<a href="#id"></a>`
    > <a href="https://google.com" target="_blank" >구글링크이올시다</a>

- `<img src="https://www.shutterstock.com/image-photo/surreal-concept-roll-world-dice-260nw-1356798002.jpg height="200" width="200" alt="this image contains a dice">`: 이미지 디스플레이 태그, alt는 대안 텍스트를 의미한다. 이미지가 제대로 디스플레이 되지 못 했을 때 alt 텍스트가 나온다.
    > <img src="https://www.shutterstock.com/image-photo/surreal-concept-roll-world-dice-260nw-1356798002.jpg" height="200" width="200" alt="this image contains a dice"> 200*200 image
- `<br>` : 라인 브레이크, 엔터, 뉴라인
    > 이제 br이 나올겁니다<br>이제 br이 나왔습니다
- `<pre></pre>`: 이 안에서 엔터 쳐도 디스플레이됨. preformatted style로 텍스트 디스플레이, 기존 텍스트 그대로 보존하여 디스플레이
    > <pre>이게 프리다. 이말이다.   탭 쳤다. <br> 엔터는 아니고 br쳤다 이말이야. 근데 실제로 엔터쳐도 된다 이말이야.</pre>
- `<hr>`: 가로지르는 라인, horizontal rule
    > hr 나오기 전<hr>hr 나온 후

- `<strong></strong>`
    > <strong>강한태그, 중요한 내용</strong>
- `<b></b>`
    > <b>볼드 태그, 그냥 볼드체</b>
- `<em></em>`: emphasize
    > <em>강조다 이말이야, 중요한 내용</em>
- `<i></i>`: 이탤릭
    > <i>이탤릭, 육성이나 느낌적인 거 표현할때 쓰자, 스타일리쉬</i>
- `<mark></mark>`
    > <mark>마크다 이말이야, 중요한 내용</mark>
- `<del></del>`
    > <del>델리트다 이말이야</del>
- `<ins</ins>`
    > <ins>인서트다 이말이야</ins>
- `<small></small>`
    > <small>작디 작은 스몰</small>
- `O<sub>2`: subscripted, 아래 첨자
    > O<sub>2
- `7<sup>3`: superscripted, 위첨자
    > 7<sup>3
- `<!-- 주석이올시다 -->` 디스플레이 상에 안나타남
- `<a href="상대주소, 로컬 주소"></a>`로도 활용 가능
- `<a href="mailto:wjdwltmd1151@gmail.com"> 필자에게 메일 보내기 </a>`
    > <a href="mailto:wjdwltmd1151@gmail.com"> 필자에게 메일 보내기 </a>
- `<head></head>`: html 안에 body 위에 보통 적으며, 콘텐츠가 아닌 내용 이 들어감. 콘텐츠는 바디에 들어감.
- `<title></title>`: head 태그 내에 적으며, 브라우저의 탭창의 이름임.

**`파비콘 (favicon)`**: 브라우저 탭창에 보이는 해당 탭의 아이콘 같은 이미지.
- `<link rel="icon" href="https://cdn4.iconfinder.com/data/icons/logos-brands-5/24/freecodecamp-512.png">`: 파비콘 이미지 설정, 헤드 태그 내에 적음

- `<table> <tr><th><th></tr> <tr><td></td></tr> </table>`: 표, table row 행, table heading 테이블 제목, table data, th의 어트리뷰트로 `scope="row"`와 `scope="col"`을 둘 수 있으며, 각각 행과 열에 대한 heading임을 나타낸다.(기능적으로 하는 건 없어보이지만, 코드상 명확히 할 수 있는듯) td의 attribute `colspan="2"`는 한 td가 2칸 영역을 차지하게 한다. 이와 유사하게 `rowspan="2"`도 적용된다. table의 td row(tr)들을 `<tbody></tbody>`로도 섹션화 할 수 있다. 마찬가지로 th row에 대해 `<thead></thead>`로도 섹션화할 수 있다. column th를 섹션화 할 때는 scope 어트리뷰트를 활용한다. tbody가 있듯이, `<tfoot></tfoot>`도 존재하는 데, tfoot은 테이블의 하단부를 섹션화할 때 사용한다.
    > <table><tr><th>이름</th><th>나이</th><th>클래스</th></tr><tr><td>토미</td><td>19</td><td>12</td></tr><tr><td>존</td><td>30</td><td>15</td></tr></table>
- `<ul> <li></li> <li></li> <li></li> </ul>` : unordered list
    > <ul> <li>리스트 1</li> <li>리스트 2</li> <li>리스트 3</li> </ul>
- `<ol> <li></li> <li></li> <li></li> </ol>` : ordered list
    > <ol> <li>리스트 1</li> <li>리스트 2</li> <li>리스트 3</li> </ol>
- `<dl> <dt></dt><dd></dd> <dt></dt><dd></dd> <dt></dt><dd></dd> </dl>` : description list, description term, description definition
    > <dl> <dt>리스트 1</dt><dd>리스트 1이다.</dd> <dt>리스트 2</dt><dd>리스트 2이다.</dd> <dt>리스트 3</dt><dd>리스트 3다.</dd> </dl>
- `<div></div>`: division, 섹션, 그룹
    ~~~
    <div style="color:green; background-color: blue;">
        <h1>First div</h1>
        <p>This is <b>bold one</b></p>
    </div>

    <div style="color:red; background-color:purple;">
        <h2>Another one</h2>
        <b>Hi</b>
    </div>
    ~~~
    아래는 구현 예시)
    <div style="color:green; background-color: blue;">
        <h1>First div</h1>
        <p>This is <b>bold one</b></p>
    </div>

    <div style="color:red; background-color:purple;">
        <h2>Another one</h2>
        <b>Hi</b>
    </div>
    이게 디브다! (레플잇 상에선 h1과 h2 텍스트도 색상이 바뀌었다.)
- `<iframe src="https://google.com" height="300" width="300" style="border: none"> </iframe>`: inline frame, 임베딩된 외부 웹페이지
    ><iframe src="https://google.com" height="300" width="300" style="border: none"></iframe>

- `&euro;`
    > &euro;
- `&dollar;`
    > &dollar;
- `&#169;`: copyright
    > &#169;
- `&#174;`: registered in U.S. patent
    > &#174;
- `&#9824;`
    > &#9824;
- `&#9827;`
    > &#9827;
- `&#9829;`
    > &#9829;
- `&#9830;`
    > &#9830;
- `&#8482;` : TradeMark
    > &#8482;

그러나 위처럼 숫자 코드로 입력하는 것보다 다이렉트로 쓰는 것이 좋은 컨벤션이다.
- `<form> <label for="username">Name</label><br><input type="text" name="username" id="username"><br><label for="school">School</label><br> <input type="number" name="school" id="school"> </form>`: 디스플레이 상의 이름은 Name인 반면, 코드 상의 인풋을 식별하기 위한 것은 <b>name="username"</b>이다. for 어트리뷰트는 라벨과 form을 연관짓기 위한 것으로 라벨을 클릭하면 바로 form으로 이어지게 한다(for과 id가 같아야 한다). 
    > <form> <label for="username">Name</label><br><input type="text" name="username" id="username"><br><label for="school">School</label><br> <input type="number" name="school" id="school"> </form>
input tag에서의 name attribute는 자바스크립트 상에서 form element를 식별하기 위한 것이고, id 어트리뷰트는 페이지에서 유일한 엘리먼트를 식별하기 위한 것이다.(솔직히 크게 둘이 뭔 차이 있는지 모르겠다.)

- `<form><input type="checkbox" value="checked"></form>`: 체크하면 checked라는 밸류가 서버로 전달된다.
    > <form><input type="checkbox"></form>
- `<form><input type="radio" value="checked"></form>`: 동그라미 체크박스(라디오 타입)
    > <form><input type="radio" value="checked"></form>
- `<form action="~~.html"><input type="submit" value="send"></form>`: 제출을 하면 action attribute에 해당하는 URL이나 위치로 form 정보가 이동한다. 일반적으로 form으로 여러 정보를 받은 뒤 마지막 input 태그로 submit 타입을 받아 form에 담긴 인풋 정보들을 서버로 넘긴다.
    > <form action=""><input type="submit" value="send"></form>
- `<form action="form.html" method="POST"></form>`
- `<form action="form.html" method="GET"></form>`

GET과 POST(method)는 HTTP 리퀘스트에 포함되는 HTTP 동사이다. GET과 POST의 차이는 아직 상세히 다루지는 않는다. 간단히 차이점을 생각해보자. 구글에 검색했을 때 검색 문구가 URL에 들어간다면 GET을 써야할 때고, POST 메소드는 일반적으로 눈에 보이지 않는다. 좀 더 자세히는 GET을 쓰면 URL을 통해 입력한 걸 보내고, POST를 쓰면 URL을 통해 전송하는 게 아니라 "request body"(리퀘스트 본문)을 전송하기 때문에 비가시적이다. GET은 데이터 전송에서 제한적인 경우가 많은 반면 POST는 좀 더 다양한 넓은 범위의 정보를 전송할 수 있다.
- password input with `<input type="password">`
    > ref: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password
    ><input type="password">
- number input form with `<input type="number">`
    > ref: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number
    ><input type="number">
- range input form with `<input type="range">`
    > ref: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range
    > <input type="range">
- dropdown list with `<select><option></option> <option></option> </select>`
    > ref: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select
- datalist input with `<datalist><option></option><option></option></datalist>`
    > ref: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist

- textarea `<textarea id="extra" name="extra" rows="3" cols="40">default message</textarea>`
    > <textarea id="extra" name="extra" rows="3" cols="40">default message</textarea>
### HTML Form validation
- required: input tag에 attribute로 두면, 빈칸으로 submit 할 수 없게 함.
- min & max: number typed input에 설정할 수 있음.
- minlength & maxlength: text typed input에 설정할 수 있음.
- matching pattern -> RegEx
    > ref: https://www.codecademy.com/resources/docs/javascript/regexp?page_ref=catalog
    > ex) **`<input type="text" pattern="[a-zA-Z0-9]+">`**
### Semantic HTML
semantic HTML이란, 의미(semantic)와 관련 있는 HTML을 작성하는 것이다.
HTML을 의미론적(시맨틱)으로 작성해야 하는 이유는 
- 코드 이해가 쉽고,
- 검색 엔진 최적화(SEO, Search Engine Optimizaiton)로 검색 상위 문서로 올라오기 위해
- 문제가 생겼을 때 브라우저가 코드를 더 잘 이해해 디스플레이에 제대로 해석되어 올라가 접근성을 높일 수 있기 때문이다
<img src="https://content.codecademy.com/courses/updated_images/SemanticVSNonSemantic_Diagram_Updated_1.svg">
왼쪽이 Non-Semantic HTML 오른쪽이 Semantic
div 태그를 용도에 따라 다음 아래 태그들로 전환하는 게 좀 더 semantic 함.

- header 태그 -> 초반 도입 내용, 인덱스 칸

- nav 태그 -> 링크 내용(목차, 색인, 인덱스)

- main 태그 -> 본내용

- footer 태그 -> 마무리 내용, 출처(레퍼런스), contacts 정보

- section 태그 -> 도큐먼트의 일부(챕터 단위, 부분 단위)

- article 태그 -> 의미 있는 텍스트 단락들 묶는 태그(독자가 읽고 이해하는 부분) 보통 주내용

- aside 태그 -> 보조 내용으로, 추가 정보 덧붙이며 주내용 보조하는 역할하는 내용

- figure 태그 -> 다이어그램, 코드 엘리먼트, 이미지, 일러스트 감싸는 태그
    - figcaption 태그 -> figure 태그 안에서 이미지 설명하는 메시지 들어감. 이미지와 함께 움직이고 이미지 바로 근처에 있도록 하는 메시지

- audio 태그 -> audio 콘텐츠(`<source src="" type="audio/mp3">`) 담는 태그, controls 속성은 컨트롤 부분을 디스플레이함. 

- video 태그 -> 비디오 콘텐츠 담는 태그
    - controls 속성
    - autoplay 속성
    - loop 속성
    등 기타 속성들은 mdn 참고


<!-- Add HTML tags and examples -->

## Learn CSS
추가적으로 codecademy의 css 배우기 시리즈 "https://www.codecademy.com/courses/learn-css/" 를 통해 css에 대해 공부하는 것을 추천함. 

Cascading Style Sheet (계단식 스타일 시트)다.
레플잇의 index.html에서 벗어나 style.css를 보자.
~~~
html {
  height: 100%;
  width: 100%;
}
~~~
~~~
<!DOCTYPE html>
<html>

<head>
  <title>My Page</title>
  +<link rel="stylesheet" href="style.css">+

<body>
  Hello world
</body>

</html>
~~~
---
<pre>
    #welcome { /*-> for id="welcome" of tags, 이건 unique
      background-color: green; */
    }
    h1.heading { /* -> for class="heading" of h1 tags, non-unique */
      color: blue;
    }
    * { /* universal selector */
      color:red;
    }
</pre>

~~~
h1 {
  color: green;
}

p {
  color: green;
}
~~~
를 아래처럼 쓸 수 있음!
~~~
h1, p {
  color: green;
}
~~~

~~~
body {
  background-image: url("https://cdn4.iconfinder.com/data/icons/logos-brands-5/24/freecodecamp-512.png");
  background-repeat: no-repeat;
  background-position: right top;
}
~~~
백그라운드 이미지도 설정할 수 있음요.


## Learn JS
## Create Frontend Movie App
## Create Backend Review App
## Connect Frontend with Backend