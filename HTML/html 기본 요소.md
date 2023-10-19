# HTML 기본 요소

## **HTML 링크(Link)란?**

- 오늘날 웹 페이지에는 다른 페이지나 다른 사이트로 연결되는 수많은 하이퍼 링크(hyperlink)가 존재합니다.
  이러한 하이퍼 링크를 간단히 링크(link)라고도 부르며, HTML에서는 `<a>`태그로 표현합니다.

  ```html
  <a href="링크주소">HTML 링크</a>
  ```

- `<a>`태그의 href 속성은 링크를 클릭하면 연결할 페이지나 사이트의 URL 주소를 명시합니다.
- `<a>`태그는 텍스트나 단락, 이미지 등 다양한 HTML 요소에 사용할 수 있습니다.

  ```html
  <a href="/html/intro">
    <h2>이 링크를 클릭해 보세요!</h2>
  </a>
  ```

---

## target 속성

- `<a>`태그의 target 속성은 링크로 연결된 문서를 어디에서 열지를 명시합니다.
  | target 속성값 | 설명 |
  | ------------------ | ---------------------------------------------------------------- |
  | \_blank | 링크로 연결된 문서를 새 창이나 새 탭에서 오픈. |
  | \_self | 링크로 연결된 문서를 현재 프레임(frame)에서 오픈. (기본설정) |
  | \_parent | 링크로 연결된 문서를 부모 프레임(frame)에서 오픈. |
  | \_top | 링크로 연결된 문서를 현재 창의 가장 상위 프레임(frame)에서 오픈. |
  | 프레임(frame) 이름 | 링크로 연결된 문서를 지정된 프레임(frame)에서 오픈. |

```html
<h2><a href="/html/intro" target="_blank">blank</a></h2>

<h2><a href="/html/intro" target="_self">self</a></h2>

<h2><a href="/html/intro" target="_parent">parent</a></h2>

<h2><a href="/html/intro" target="_top">top</a></h2>

<h2><a href="/html/intro" target="myframe">myframe</a></h2>

<iframe name="myframe" style="width:50%; height: 330px"></iframe>
```

- HTML 프레임(frame)에 대한 더 자세한 사항은 HTML iframe 요소 수업에서 확인할 수 있습니다.

## 링크의 상태(state)

- HTML 링크의 상태는 다음과 같이 네 가지로 구분할 수 있습니다.
  | 링크의 상태 | 설명 |
  | ----------- | --------------------------------------------- |
  | link | 아직 한 번도 방문한 적이 없는 상태 (기본설정) |
  | visited | 한 번이라도 방문한 적이 있는 상태 |
  | hover | 링크 위에 마우스를 올려놓은 상태 |
  | active | 링크를 마우스로 누르고 있는 상태 |
- 웹 브라우저에서 링크가 연결되어 있는 텍스트의 색상은 다음과 같습니다.

  - 기본적으로 링크가 걸린 텍스트는 밑줄에, 텍스트 색상이 파란색으로 변경됩니다.
  - visited 상태의 링크는 밑줄에, 텍스트 색상이 보라색으로 변경됩니다.
  - active 상태의 링크는 밑줄에, 텍스트 색상이 빨간색으로 변경됩니다.

    ```html
    <style>
      a:link {
        color: teal;
      }

      a:visited {
        color: maroon;
        text-decoration: none;
      }

      a:hover {
        color: yellow;
        text-decoration: none;
      }

      a:active {
        color: red;
        text-decoration: none;
      }
    </style>
    ```

---

## HTML 이미지(Image)

- 이미지(image)란 2차원 평면 위에 그려진 시각적 요소를 의미합니다.
  오늘날 웹 페이지에는 이러한 이미지가 매우 중요한 요소의 하나로 자리 잡고 있습니다.
- 웹 페이지에서 주로 사용되는 이미지의 종류는 다음과 같습니다.

- PEG
  [다운로드 (1).jfif](<https://s3-us-west-2.amazonaws.com/secure.notion-static.com/49f3e32b-e634-443e-9871-97a62d5f79c5/%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C_(1).jfif>)
- PNG
  ![PNG 이미지.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/899b8daa-4402-4d28-853f-6be254865c58/PNG_%EC%9D%B4%EB%AF%B8%EC%A7%80.png)
- GIF
  ![gIF 이미지 자료.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/04da91da-183a-4825-9154-5132a3be1764/gIF_%EC%9D%B4%EB%AF%B8%EC%A7%80_%EC%9E%90%EB%A3%8C.gif)

## 이미지의 삽입

- HTML 문서에 이미지를 삽입할 때는 `<img>`태그를 사용합니다.
- `<img>`태그는 종료 태그가 없는 빈 태그(empty tag)이며, 다음과 같은 문법으로 사용됩니다.

  ```html
  <img src="이미지주소" alt="대체문자열" />
  ```

- src 속성은 이미지가 저장된 주소의 URL 주소를 명시합니다.
- alt 속성으로 이미지가 로딩될 수 없는 상황에서 이미지 대신 나타날 문자열을 설정할 수 있습니다.

  ```html
  <img src="/img_html5_logo.png" alt="이미지가 없나봐요.." />
  ```

---

## 이미지의 크기(width, height) 설정

- HTML에서는 style 속성을 사용하여 이미지의 크기를 설정할 수 있습니다.
  또한, width 속성과 height 속성을 이용하면, 이미지의 너비와 높이를 각각 픽셀(pixel) 단위로 설정할 수도 있습니다.
  위의 두 가지 방법 모두 HTML5 표준에는 적합한 방법이지만, 나중에 배우게 될 CSS를 이용한 내부 스타일 시트나 외부 스타일 시트와 상관없이 이미지의 원래 크기를 유지하려면 style 속성을 사용하는 것이 좋습니다.

```html
<style>
  img {
    width: 100%;

    border: 1px solid black;
  }
</style>

...

<img
  src="/examples/images/img_flag.png"
  alt="html size"
  width="320"
  height="214"
/>

<img
  src="/examples/images/img_flag.png"
  alt="style size"
  style="width:320px; height:214px"
/>
```

---

## HTML 리스트(List)

- 리스트(list)란 여러 요소들을 일렬로 나열한 목록이나 명단을 의미합니다.
  - HTML에서는 이러한 리스트를 표현하기 위해 다음과 같은 리스트를 제공하고 있습니다.
  1. 순서가 없는 리스트(unordered list)
  2. 순서가 있는 리스트(ordered list)
  3. 정의 리스트(definition list)

## 순서가 없는 리스트

- 순서가 없는 리스트는 `<ul>`태그로 시작하며, 여기에 포함되는 각각의 리스트 요소는 `<li>`태그로 시작합니다.
- 각각의 리스트 요소 앞에는 기본 마커(marker)로 검정색의 작은 원(bullet)이 위치합니다.

  ```html
  <ul>
    <li>사과</li>

    <li>멜론</li>

    <li>바나나</li>
  </ul>
  ```

- disc : 검정색 작은 원 모양 (기본설정)
- circle : 흰색 작은 원 모양
- square : 사각형 모양

  ```html
  <ul style="list-style-type: circle">
    <li>수박</li>

    <li>참외</li>

    <li>옥수수</li>
  </ul>

  <ul style="list-style-type: square">
    ...
  </ul>
  ```

- list-style-type 속성에 대한 더 자세한 사항은 CSS 리스트 수업에서 확인할 수 있습니다.

---

## 순서가 있는 리스트

- 순서가 있는 리스트는 `<ol>`태그로 시작하며, 여기에 포함되는 각각의 리스트 요소는 `<li>`태그로 시작합니다.
  각각의 리스트 요소 앞에는 기본 마커로 아라비아 숫자가 위치합니다.

  - CSS의 list-style-type 속성을 사용하면 리스트 요소 앞에 위치하는 마커(marker)를 다른 모양으로 변경할 수 있습니다.
  - decimal : 숫자 (기본설정)
  - upper-alpha : 영문 대문자
  - lower-alpha : 영문 소문자
  - upper-roman : 로마 숫자 대문자
  - lower-roman : 로마 숫자 소문자

  ```html
  <ol style="list-style-type: upper-alpha">
    <li>수박</li>

    <li>참외</li>

    <li>옥수수</li>
  </ol>

  <ol style="list-style-type: lower-alpha">
    ...
  </ol>

  <ol style="list-style-type: upper-roman">
    ...
  </ol>

  <ol style="list-style-type: lower-roman">
    ...
  </ol>
  ```

---

## 정의 리스트(description list)

- 정의 리스트(description list)는 용어와 그에 대한 정의를 모아놓은 리스트로 `<dl>`태그로 시작합니다.
  `<dt>`태그에는 용어의 이름이 들어가고, `<dd>`태그에는 해당 용어에 대한 정의가 들어갑니다.

---

## HTML 테이블(Table)란?

- 테이블(Table)이란 여러 종류의 데이터(data)를 보기 좋게 정리하여 보여주는 표를 의미합니다.
  HTML에서는 `<table>`태그를 사용하여 이러한 테이블을 작성할 수 있습니다.
  `<table>`태그는 다음과 같은 태그들로 구성됩니다.

  1. `<tr>`태그는 테이블에서 열을 구분해 줍니다.
  2. `<th>`태그는각 열의 제목을 나타내며, 모든 내용은 자동으로 굵은 글씨에 가운데 정렬이 됩니다.
  3. `<td>`태그는 테이블의 열을 각각의 셀(cell)로 나누어 줍니다.

     ```html
     <table style="width:100%">
       <tr style="background-color:lightgrey">
         <th>참치</th>

         <th>고래</th>
       </tr>

       <tr>
         <td>상어</td>

         <td>문어</td>
       </tr>

       <tr>
         <td>오징어</td>

         <td>고등어</td>
       </tr>
     </table>
     ```

- CSS의 border 속성을 이용하여 테이블에 테두리를 표현할 수 있습니다.
  border 속성값을 따로 명시하지 않으면, 해당 테이블은 언제나 빈 테두리를 가지게 됩니다.

```html
<style>
  table,
  th,
  td {
    border: 1px solid black;
  }
</style>
```

- 위의 예제에서 테이블의 테두리(border)가 두 줄씩 나타나는 이유는 `<table>`태그와 `<th>`태그, `<td>`태그가 모두 자신만의 테두리를 가지고 있기 때문입니다.
- 위와 같이 두 줄로 표현되는 테두리를 한 줄로 설정하려면 border-collapse 속성을 사용해야 합니다.
- border-collapse 속성값을 collapse로 설정하면, 테이블의 테두리를 한 줄로 표현할 수 있습니다.

  ```html
  <style>
    table,
    th,
    td {
      border: 1px solid black;
      border-collapse: collapse;
    }
  </style>
  ```

---

## 테이블의 열 합치기

- colspan 속성을 사용하면 테이블의 열(column)을 합칠 수 있습니다.

  ```html
  <table style="width:100%">
    <tr>
      <td>참치</td>

      <td colspan="2">고래</td>
    </tr>

    <tr>
      <td>상어</td>

      <td>문어</td>

      <td>꽁치</td>
    </tr>
  </table>
  ```

## 테이블의 행 합치기

- rowspan 속성을 사용하면 테이블의 행(row)을 합칠 수 있습니다.

  ```html
  <table style="width:100%">
    <tr>
      <td rowspan="2">상어</td>

      <td>문어</td>

      <td>꽁치</td>
    </tr>

    <tr>
      <td>고등어</td>

      <td>돌고래</td>
    </tr>
  </table>
  ```

## 테이블의 열과 행 합치기

- colspan 속성과 rowspan 속성을 함께 사용하면, 더욱 복잡한 테이블도 표현할 수 있습니다.

  ```html
  <table style="width:100%">
    <tr>
      <td colspan="6">1</td>
    </tr>

    <tr>
      <td colspan="6">2</td>
    </tr>

    <tr>
      <td rowspan="3">3</td>

      <td rowspan="3">4</td>

      <td colspan="2">5</td>

      <td>6</td>

      <td>7</td>
    </tr>

    <tr>
      <td colspan="3">8</td>

      <td>9</td>
    </tr>

    <tr>
      <td colspan="4">10</td>
    </tr>
  </table>
  ```

## 테이블의 캡션(caption) 설정

- `<caption>`태그를 사용하면 테이블 상단에 제목이나 짧은 설명을 붙일 수 있습니다.

  ```html
  <table style="width:100%">
    <caption>
      해양 생물
    </caption>

    <tr>
      <td>참치</td>

      <td>고래</td>

      <td>날치</td>
    </tr>
  </table>
  ```

---
