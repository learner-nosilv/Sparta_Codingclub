# 📁 Web_basic → [(사전) 웹개발종합반](https://spartacodingclub.kr/online/web_basic)

- 노션 토글열기 `ctrl + alt + T`
- 뼈대자동완성 `! + ↵` 혹은 `html:5 + ↵`
- 파일브라우저열기 `alt + B`
- [커밋합치기](https://naradesign.github.io/git-commit-fixup-squash.html) `git rebase -i HEAD~갯수`

## **1주차** | HTML/CSS기초

- 태그는 외우는 것이 아니고 검색해서 가져다가 쓰는 것이다
- CSS는 요소(element)에 명찰을 붙이고 그 명찰을 부르는 형식으로 꾸밀 수 있다.
- 오타나니까 자동완성이 가능한 것들은 굳이 타이핑하지말고 `tab`으로 자동완성하기
- **사용한 Tags** : `div 구획나누기` `h1~6제목` `input입력창` `button`
- **사용한 CSS properties**
  - `width` `height` `color` `background-color`
  - `border-radius` `margin경계밖공백` `padding경계안공백`
    - **value**: `auto 끝까지민다`
  - 배경이미지SET `background-image` `background-size` `background-position`
  - `box-shadow: 0px 0px 3px 0px blue;`
- 여러 요소를 같이 이동시키려면 : 박스 씌우기 (e.g. `<div>`)
  - 박스를 만들때는 박스범위를 모르니 `background-color:green;` 로 가시화해주기
- 무언가를 가운데 둔다는 것 = 양쪽마진을 최대한 동등하게 밀어두는 것
  - 끝까지 민다`auto`를 사용 ! e.g. `margin: 20px auto 0px auto;`
- 박스 속 모든 내용물 정렬
  - `display: flex;` 플렉스박스로 만들겠음
  - `flex-direction: column;` 아이템-정렬:세로로
  - `justify-content: center;`
  - `align-items: center;`
- 남이 만들어 놓은 예쁜 CSS 꾸러미 → `Bootstrap`  
  ( _붓을 쥘 줄 아는 것과 그림을 예쁘게 그릴 줄 아는 것은 다른 겁니다._ )

### 1주차 실습 | 추억앨범

1. `Bootstrap` 추가하기
2. `googlefont` 사용하여 원하는 font import 후 CSS로 **전체 적용**
   - `* { font-family: '폰트명', '폰트명2', sans-serif; }`
3. ① 나만의 추억앨범 헤더 파트
   - HTML & CSS 구현 : 배웠던 CSS들 전부 활용
4. ③ 4열로 나열된 앨범카드 파트
   - `Bootstrap` 의 Card 카테고리 활용
5. ② 앨범 포스팅 박스 파트 | bootstrap 활용하여 구현
   - 박스 그림자 구현 `box-shadow: 0px 0px 3px 0px blue;`
   - 안쪽 여백 생성 `padding: 20px;`
   - `Bootstrap` 의 forms, buttons 카테고리 활용

![Chap.1 result](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/1%EC%A3%BC%EC%B0%A8-%EC%BD%94%EB%94%A9%EA%B2%B0%EA%B3%BC.png?raw=true)

│

## **2주차** | Javascript

### **1주차 복습** | [Spartaflix](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/%232-1%20SpartaFlix.html)

1. `Bootstrap` 추가하기
2. `googlefont` 사용하여 원하는 font import 후 CSS로 **전체 적용**
   - CSS `* { font-family: '폰트명', '폰트명2', sans-serif; }`
3. 화면을 검정색으로 구현
   - CSS `body { background-color: black; }`
4. `HTML` 수정 및 배웠던 `CSS`들 전부 활용하여 목표대로 구현하기!
5. ① 헤더 네비게이션 바 | HTML & CSS 구현
   - `Bootstrap` 의 Examples → Headers 활용
6. ② 메인 영화 점보 헤더 | bootstrap 활용하여 구현
   - `Bootstrap` 에서 jumbotron 검색한 후 `F12`로 `HTML` 복사
   - 버튼복사, 클래스 생성, text기입 등 목표에 맞게 `HTML` 수정
   - 배경이 특정 영화 이미지가 되도록 `CSS` 수정
     - `background-image: url('영화이미지URL');`
     - `background-position: center;`
     - `background-size: cover;`
7. ③ 영화 포스팅 박스 파트 | bootstrap 활용하여 구현
   - 박스 그림자 구현 `box-shadow: 0px 0px 3px 0px gray;`
   - 안쪽 여백 생성 `padding: 20px;`
   - bootstrap의 forms, buttons, input group 카테고리 활용
8. ④ 4열로 나열된 영화소개 카드 파트
   - bootstrap 의 Card 카테고리 활용
   - 클래스 수정 `row-cols-md-3 g-4` → `row-cols-md-4 g-4` (3행→4행)
   - HTML로 별점 요소 추가 `<p class="card-text">⭐</p>`

![Chap.2 result](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/2%EC%A3%BC%EC%B0%A8-1%EC%A3%BC%EC%B0%A8%EB%B3%B5%EC%8A%B5-%EC%BD%94%EB%94%A9%EA%B2%B0%EA%B3%BC.png?raw=true)

### Javascript : PL/움직임부여/서버통신

- 브라우저 조작을 JS만 할 수 있는 것은 아니지만, 많은 사람들이 오래 사용하면서 JS가 표준이 되었다!
- 변수 선언 및 초기화 : `let 변수명 = 변수값 ;`
- Console에 값 출력 : `console.log(변수명) ;`
  - 왜 출력? 보통은 개발자의 원활한 개발을 위해서
- 알림창 띄우기 : `alert('알림내용') ;`
- **유용한 변수의 형태 ① list**
  - 선언 : `let 변수명 = [값0, 값1, ];`
  - 사용 : `변수명[Index];`
  - 장점 : 하나의 이름으로 수 백개의 값을 줄줄이 가지고 다닐 수 있음
  - 의의 : 개별 이름을 붙여줄 필요가 없는 비슷한 계열의 값들을 많이 사용해야 할 때 사용
- **유용한 변수의 형태 ② dictionary**
  - 선언 : `let 변수명 = {'키1':값1, '키2':값2, };`
  - 사용 : `변수명[키];`
  - 장점 : list의 특성을 가져가면서도 (키:값) 쌍으로 구성되어 Index가 아닌 키를 통해 특정 값에 접근할 수 있음
  - 의의 : 한 개체가 여러 속성과 속성값을 가질 때 사용

> 코딩을 하면서 문법의 규칙을 일원화하려고 생각하시면 절대 안됩니다.
>
> - 꺾쇠는 어디에 쓰는거고... 중괄호는 어디에 쓰는거고... 이렇게 시작을 하면 절대로 코딩을 이해하거나 쉽게 잘해지기가 어렵습니다. 왜냐면요 그렇게 만들어지지 않았거든요.  
>   _"[ ] 는 언제쓰더라?"_ 이렇게 하면 안돼요.
> - _"Dict에서 값을 가지고 나올 때 [ ]를 쓴다"_ 이렇게 이해해야해요. 통단위로 이해해주세요.

- **조건문** : `if (조건) { 실행문 }` `else { 실행문 };`
- **반복문** : `원소를 계속 하나씩 꺼내서` 반복해라

```javascript
// 조건문, 반복문 둘 다 사용 예

let ages = [15, 30, 11, 25, 65, 13, 21, 32];  // 8개의 원소를 둔 리스트
let i = 0;

// [반복문] ages 리스트에서 원소를 맨 앞부터 하나씩 꺼내어 element에 저장
//         원소가 더 이상 나오지 않을 때까지 { }을 반복
ages.forEach((`element`) => {
  i += 1;
  // [조건문] 원소의 값이 20이하일 때만 청소년 출력, 그 외 성인
  if (element < 20) {
    console.log("[" + i + "] 나이 " + element + "살 : 청소년입니다.");
  }
  else {
    console.log("[" + i + "] 나이 " + element + "살 : 성인입니다.");
  }
});
```

- **함수**
  - 선언 `function` _함수명_`()` `{` _내용_ `}`
  - 사용 예 `<button onclick="`_함수명_`()">` - 이 버튼 클릭 시, 이 함수 호출
- html에서 특정 요소의 내용을 '안녕'으로 바꾸는 javascript 명령어
  - `document.getElementById('ID명').innerHTML = '안녕';`
    - `document` html문서 ─ `.` ~의 ─ `getElementById('□')` 해당 ID를 가진 요소
    - → 이렇게 순수 JS로 길게길게 작성하는 것이 귀찮은 사람들이 JS를 미리 적어놓고 그걸 간단하게 호출해서 사용하기 시작함 **[Library]**
- **JQuery** ← 누군가 만들어놓은 일종의 Javascript Library
  - JQuery를 사용하는데에 필요한 미리 적어놓은 JS 덩어리를 임포트해야 JQuery를 사용할 수 있음
    - `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>`
  - `document.getElementById('ID명').innerHTML = '안녕';` 를 JQuery로 구현? `$('#ID명').html('안녕');`
  - Selector `{'#ID명'}`
  - 사용 예 : ID가 q1인 **요소의 내용을** 사과로 **바꾸기**
    - `$('#q1').text('사과');`
  - 사용 예 : profile의 **html에** **변수**name**의 값을** 내용으로 하는 문단요소 **넣기**
    - `let profile = <p>이름은 ${name}</p>` (값을 백틱으로 묶기)
  - 사용 예 : ID가 q2인 **요소 속 html에** profile의 내용을 덧붙이기\*\* - `$('#q2').append(profile)` -
    │

## **3주차** | Javascript

### 3(1) - 2주차 복습 | JQuery를 활용하여 포스팅 박스에 입력한대로 새 카드를 추가하는 기능 구현

| ![Chap.3 review result](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/3%EC%A3%BC%EC%B0%A8-2%EC%A3%BC%EC%B0%A8%EB%B3%B5%EC%8A%B5-%EC%B6%94%EC%96%B5%EC%95%A8%EB%B2%94%EC%97%90%20JQuery%EB%A1%9C%20%EA%B8%B0%EB%8A%A5%EB%84%A3%EA%B8%B0.png?raw=true)[추억앨범 결과](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/%233-1%20Album-JQuery.html) | ![Chap.3 review result](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/3%EC%A3%BC%EC%B0%A8-2%EC%A3%BC%EC%B0%A8%EB%B3%B5%EC%8A%B5-%ED%94%8C%EB%A6%AD%EC%8A%A4%EC%97%90%20JQuery%EB%A1%9C%20%EA%B8%B0%EB%8A%A5%20%EB%84%A3%EA%B8%B0.png?raw=true)[Spartaflix 결과](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/%233-2%20SpartaFlix-JQuery.html) |
| :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |

1. 특정 버튼을 누르면, 포스팅 박스 열고 닫히도록 하는 기능
   - 포스팅 박스에 id 생성
     - `<div id="posting-box"> ··· </div>`
   - 포스팅 박스를 열고 닫는 기능의 함수 구현
     - `function openclose() { $('#posting-box').toggle(); }`
   - 특정 버튼을 클릭할 때 위 함수가 작동되도록 구현
     - `<button onclick="openclose()"> ··· </button>`
2. 포스팅 박스에 내용을 입력하고 기록 버튼을 누르면 그 내용대로 새 카드가 추가되도록 하는 기능
   - 포스팅 박스 속 입력 박스 각각, 카드뭉치박스에 id 생성
     - `<input type="email" id="image" ··· />`
     - `<div id="cardSet">`
   - 카드뭉치의 html에 입력한 내용대로 새로운 카드 html을 덧붙이는 함수 구현
     - `function addCard() {`
     - `  let image = $('image').val();`
     - `  let temp_html = 백틱 카드생성 HTML들 수정`
     - `     <img src="${image}" ··· 백틱;`
     - `  $('#cardSet').append(temp_html); }`
   - 특정 버튼을 클릭할 때 위 함수가 작동되도록 구현
     - `<button onclick="addCard()"> ··· </button>`

### 3(2) - Client ↔ Server

- **Server** `은행` Client가 요청하는 자료 뭉치들을 전부 가지고 있는 곳
- **API** `예금, 상담 등 창구` Client의 특정 자료 요청만을 수행/제공하는 곳
- **HTML이 웹에 구현되면 자동으로 실행할 코드**
  - `$(document).ready(function () { ··· } );`
- `JSon` Server/API가 제공하는 데이터의 형식 중 하나≒`Dictionary`
- `Fetch` : API에게 자료를 요청해서 받아오는 방법
  - Client가 API에게 데이터를 요청하는 방식 2가지
    - ① `GET` `URL`에 요청에 필요한 데이터를 포함하는 방식
      - `https:// 서버주소 / API주소 ? 속성명=값 & 속성명=값 & ···`
    - ② `POST` `data : { 속성명: 값, 속성명: 값, ···}`으로 데이터를 포함하는 방식
  - `fetch("요청URL")`.`then(result => result.json())`.`then(json_result => { json_result를 활용하는 코드; })`
    1. `fetch("요청URL")` 이 URL에 get방식으로 웹 통신 요청
    2. `then(result ` 그 후에 받은 데이터가 있다면 result라는 이름을 붙이고 =>
    3. `=> result.json())` => 그 result를 json 형식으로 바꾸기
    4. `then(json_result` 그 후에 받은 데이터에 json_result라는 이름을 붙이고 =>
    5. `=> { json_result를 활용하는 코드; })` => 그 json_result를 사용하는 코드를 실행하기
       - (예) `let elements = json_result['list']['person'];`
       - `    elements.forEach( (person) => {console.log(person)} );`

### 3-(3) 3주차 실습 | open API 활용하여 실시간 서울 미세먼지 정보와 기온 표시하기

```javascript
$(document).ready(function () {
  // 웹 구현시 자동 실행
  let url =
    "http://openapi.seoul.go.kr:8088/6d4d776b466c656533356a4b4b5872/json/RealtimeCityAir/1/99";

  fetch(url)
    .then((res) => res.json())
    .then((data) => {
      let mise = data["RealtimeCityAir"]["row"][0]["IDEX_NM"];
      $("#mise_info").text(mise); // 해당 요소의 content를 변수 mise의 값으로 변경
    });
});
```

| ![결과사진](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/3%EC%A3%BC%EC%B0%A8-%EC%B6%94%EC%96%B5%EC%95%A8%EB%B2%94%EC%97%90%20%EC%84%9C%EC%9A%B8%20%EB%AF%B8%EC%84%B8%EB%A8%BC%EC%A7%80%20%EC%8B%A4%EC%8B%9C%EA%B0%84%20%EC%95%88%EB%82%B4%ED%95%98%EA%B8%B0.png?raw=true)[앨범 결과](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/%233-5%20Album-fetch.html) | ![결과사진](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/3%EC%A3%BC%EC%B0%A8-%ED%94%8C%EB%A6%AD%EC%8A%A4%EC%97%90%20%EC%84%9C%EC%9A%B8%20%EA%B8%B0%EC%98%A8%20%EC%8B%A4%EC%8B%9C%EA%B0%84%20%EC%95%88%EB%82%B4%ED%95%98%EA%B8%B0.png?raw=true)[Spartaflix 결과](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/%233-6%20SpartaFlix-fetch.html) |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |

## **4주차** | Firebase의 Firestore Database

- `FE` 서버로 데이터를 전송하는 작업
- `BE` 받은 데이터를 잘 저장하는 작업, 서버 구축/관리 및 데이터를 검색, 인출하는 작업
- `Database` 데이터들의 모음, 저장/인출/색인 등 데이터를 관리하기 용이함

  - `Relational DB(SQL)` 모든 정보가 동일한 속성/필드를 가짐(값은 다름)
  - `Non-Relational DB(NoSQL)` 정보들이 다른 속성/필드를 가질 수 있음(Not only SQL)

- `Firebase` 백엔드가 하는 일을 대신 해주는 구글의 웹/앱 개발 플랫폼
  - Firestore database 클라우드기반 NoSQL DB
  - Collection ⊃ Document ⊃ Field
- 사용법 ① Firestore database 세팅하기 | 내 인증키 필요

  ```javascript
  <script type="module">    // script 타입설정 → onclick="함수명()" 작동 X

  // Firebase SDK 라이브러리 가져오기
  import { initializeApp } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-app.js";
  import { getFirestore } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-firestore.js";
  import { collection, addDoc } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-firestore.js";
  import { getDocs } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-firestore.js";

  // Firebase 구성 정보 설정
  const firebaseConfig = { 본인 설정 내용 채우기 };

  // Firebase 인스턴스 초기화
  const app = initializeApp(firebaseConfig);
  const db = getFirestore(app);

  </script>
  ```

- 사용법 ② script type이 "module"이 되면 onclick 속성이 작동되지 않으므로, JQuery를 이용하여 해당 기능을 가진 함수 작성하기 [동적 제작]
  - `$("#누를 버튼의 ID").click( async function (){버튼 클릭 후, 작동될 코드들;} );`
    - async(Asynchronous) : 비동기 작업, 다른 작업의 완료여부와 상관없이 작동
- 사용법 ③ 입력받은 값을 DB에 저장하기
  - `await addDoc(collection(db, "콜렉션이름"), { 키: 값, 키: 값, ··· });`
    - await ≒ 잠시 로딩을 멈춘 후 DB사용부터 하기
  - 저장 후 화면 새로고침 `window.location.reload();`
- 사용법 ④ DB에서 값을 인출하기
  - let items = `await getDocs(collection(db, "콜렉션이름"));`
  - `items.forEach( (item)=>{ ··· } );` 등 으로 가공하기

### 4주차 실습, 5주차 복습 | 추억앨범, Spartaflix의 포스팅 박스에 Firestore의 Firebase를 연결하기

① Firebase SDK 라이브러리 임포트하고 세팅하기

② 버튼 클릭 시 입력받은 데이터를 DB에 저장하는 기능

- `$('#클릭할 버튼ID').click(async function) { □ };` 속에 작성
- 입력받은 데이터 딕셔너리화
  - `let post = { title : $('#제목인풋박스의ID').val(), ··· };`
- DB저장 `await addDoc(collection(db, "album혹은movie"), post);`
- 완료팝업 후 페이지 새로고침 `alert("저장성공!");` `window.location.reload();`

③ 화면 로드 시 DB의 데이터들을 읽고 카드형식으로 만드는 기능

- `<script type="module">` 이므로 화면로드 후 자동으로 수행됨
- DB인출 `let posts = await getDocs(collection(db, "album혹은movie"));`
- 인출한 데이터 개별 가공 : `posts.forEach( (post)=>{□} );` 속에 작성
  - `let item = post.data();`
  - `let title = item['title'];` `let star = "⭐".repeat(item['star']);`
  - 기존 카드 생성 HTML에 DB값이 반영된 새 카드 HTML 추가하기
    - `let tempHtml = 백틱 ··· 카드HTML 복붙 후 수정 <h5 class="card-title">${title}</h5> <p>${star}</p> ··· 백틱;`
    - `$('#cardSet').append(tempHTML);`

| ![추억앨범](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/4%EC%A3%BC%EC%B0%A8-%EC%B6%94%EC%96%B5%EC%95%A8%EB%B2%94%EC%97%90%20Firebase%EC%97%B0%EA%B2%B0%ED%95%98%EA%B8%B0.png?raw=true)[앨범 결과](<https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/%234-4%20Album-DB(%EC%A0%95%EB%B3%B4%EA%B0%80%EB%A6%BC).html>) | ![Spartaflix](https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/result_img/5%EC%A3%BC%EC%B0%A8-%ED%94%8C%EB%A6%AD%EC%8A%A4%EC%97%90%20Firebase%EC%97%B0%EA%B2%B0%ED%95%98%EA%B8%B0.png?raw=true)[Spartaflix 결과](<https://github.com/learner-nosilv/Sparta_Codingclub/blob/main/Web_basic/%235-1%20SpartaFlix-DB(%EC%A0%95%EB%B3%B4%EA%B0%80%EB%A6%BC).html>) |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |

## 5주차 | 배포 Deploy with Github 와 Python 맛보기

### Deploy

- `URL` Uniform Resource Locator
  - 리소스의 고유한 위치주소 `프로토콜://도메인/경로`
  - `Protocol` 웹 브라우저-서버간 통신방식(규약) `https`를 주로 사용
    - `https`(http+Sequrity) 통신의 중간 지점에서 통신 내용을 읽을 수 없도록 보안을 강화한 http 통신방식
  - `Domain` 사이트명.최상위도메인 (예) naver.com
  - `Path` 특정 페이지, 파일의 접근에 필요한 경로
  - (예) `https://spartacodingclub.kr/catalog`
    - 브라우저-서버는 https 프로토콜로 통신함
    - 도메인 spartacodingclub.kr 에 접근 후
    - catalog 속 정보를 브라우저가 server에 요청해서
    - 받아와서 사용자에게 웹페이지로 보여주고 있음
- `배포Deploy` 개발완료 혹은 수정한 소프트웨어를 사용자들이 사용할 수 있도록 외부에 공개하는 작업
- `Github`
  - 1. 코드 작성의 버전관리 온라인 툴
  - 2. 개발 협업 툴
  - 3. 코드 웹 호스팅 ★ → `Deploy`
    - `Github Pages` 정적 웹 페이지를 배포하는 기능 제공
  - 4. 지식공유

Github page를 통해 Spartaflix를 배포하는 작업을 해보았다.  
그런데, Firebase 개인 인증키가 코드에 들어있어서 닫았다.

`Firebase`는 백엔드가 해야할 일을 대신 해주는 대신 제약이 있다.  
→ `python`의 사용으로 유연한 서버의 구축과 관리가 가능

### Python Scraping

- `Python`을 사용하여 특정 웹페이지의 HTML을 읽어올 수 있음
- `Colab` 에서 코드를 작성하고 Ctrl+Enter로 실행
- ① Scraping용 도구 임포트하기

  ```python
  import requests
  from bs4 import BeautifulSoup

  URL = "스크래핑하려는 URL"
  headers = {'User-Agent' : 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.86 Safari/537.36'}
  data = requests.get(URL, headers=headers)

  soup = BeautifulSoup(data.content, 'html.parser')
  ```

- ② 가져온 HTML코드를 가공하여 원하는 Data만 추출하기
  - `item = soup.select_one('읽을 요소의 셀렉터')` → HTML 전부 추출
  - `item = soup.select_one('읽을 요소의 셀렉터')['attribute']` → 속성만 추출
  - `item = soup.select_one('읽을 요소의 셀렉터').text()` → content만 추출
