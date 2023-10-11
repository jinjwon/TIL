# HTML

## HTML이란?

- HTML은 HyperText Markup Language의 약자입니다.
  웹 페이지는 HTML 문서라고도 불리며, HTML 태그들로 구성됩니다.
  각각의 HTML 태그는 웹 페이지의 디자인이나 기능을 결정하는데 사용됩니다.

```<!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
  </head>
  <body>

  </body>
  </html>
```

- html 기본 구성은 이렇다.

---

## HTML 텍스트 요소

1. <태그이름> **- 시작 태그 -**
2. </태그이름> **- 종료 태그 -**

> `<img>` `<br>` `<hr>` 등과 같이 종료 태그 없이 시작 태그만을 가지는 태그를 빈 태그(empty tag)라고 합니다

### 제목

- HTML은 제목을 표현할 수 있는 다양한 크기의 `<h>`태그를 제공합니다.
  가장 큰 `<h1>`태그부터 가장 작은 `<h6>`태그까지 다양한 크기로 제목을 표현할 수 있습니다.
- `<h1>, <h2>, <h3>` 태그 제목을 표시한다

```html
<h1>제목 1크기</h1>
<h2>제목 2크기</h2>
<h3>제목 3크기</h3>
<h4>제목 4크기</h4>
```

> 💡 HTML 문서의 제목에 해당하는 부분을 `<big>`태그나 `<bold>`태그를 사용하여 표현하지 않도록 합니다.
> `<h>`태그의 위아래로는 약간의 여백이 자동으로 삽입됩니다.

---

### 단락

- 단락이란 내용상 끊어서 구분할 수 있는 하나하나의 부분을 의미하며, 문단이라고도 부릅니다.
  HTML에서는 `<p>`태그를 이용하여 이러한 단락을 표현합니다.

- `<p>`태그에 단락 넣어준다

  ```html
  <h1>제목1의 크기입니다!</h1>
  <p>단락 1</p>
  <p>단락 2</p>
  ```

- **텍스트(text) 서식 미리 정의하기**

  ```html
  <pre>
  
  줄을 나누고 싶어서
  
  이렇게 줄을 나누었다.
  
   
  
  과연     그대로     출력이     될까?
  
  </pre>
  ```

- **띄어쓰기, 수평 가로 구분선**
- 띄어쓰기

  ```html
  <br />태그(break line)를 사용하면 새로운 단락을 만들지 않고도 줄을 나눌 수
  있습니다. 이러한 <br />태그는 종료 태그가 없는 빈 태그(empty tag)입니다.
  ```

- 수평 가로 구분선

  ```html
  <p>저는 하나의 단락입니다.</p>

  <hr />

  <p>저는 하나의 단락입니다.</p>

  <hr />

  <p>저는 하나의 단락입니다.</p>
  ```

---

### 서식

- HTML은 텍스트(text)에 다양한 효과를 주는 여러 태그(tag)를 제공합니다.

- **강조 효과**
- HTML 문서에서 텍스트를 굵게 표현하고 싶을 때에는 `<b>`태그(bold text)나 `<strong>`태그를 사용하면 됩니다.

  ```html
  <p><b>"이 부분"</b>은 단순히 글씨가 굵은 부분이에요!</p>

  <p><strong>"이 부분"</strong>은 중요한 부분이라서 굵게 표현됐어요!</p>
  ```

- HTML 문서에서 이탤릭체를 표현하고 싶을 때에는 `<i>`태그(italic text)나 `<em>`태그(emphasized text)를 사용합니다.

---

- **하이라이팅 효과**
- `<mark>`태그는 텍스트에 하이라이팅(highlighting) 효과를 적용시켜 줍니다.

  ```html
  <p><mark>"이 부분"</mark>만 하이라이팅하고 싶어요.</p>
  ```

- **사입 효과**
- `<ins>`태그(insert)는 텍스트 밑에 가로줄을 만들어 마치 빈칸에 텍스트를 삽입한 것과 같은 효과를 내줍니다.

  ```html
  <p><ins>"밑줄 친 부분"</ins>에 들어갈 알맞은 말을 고르세요.</p>
  ```

### 인용구

- **짧은 인용구**
- 짧은 인용구는 <q> 태그(quotation)를 사용하여 표현할 수 있으며, 자동으로 앞뒤에 큰따옴표가 붙습니다.

  ```html
  <p><b>"이 부분"</b>은 단순히 글씨가 굵은 부분이에요!</p>

  <p><strong>"이 부분"</strong>은 중요한 부분이라서 굵게 표현됐어요!</p>
  ```

- **블록 인용구**

- 길이가 긴 인용문은 `<blockquote>`태그(block quatation)를 사용하여 표현할 수 있습니다.
- `<blockquote>`태그는 이러한 인용 부분을 별도의 단락으로 구분하여 나타냅니다.

  ```html
  <p>HTML의 정의</p>

  <blockquote>
    인터넷 서비스의 하나인 월드 와이드 웹을 통해 볼 수 있는 문서를 만들 때
    사용하는 프로그래밍 언어의 한 종류이다.
  </blockquote>
  ```

### 주석

- 주석(comment)이란 개발자가 작성한 해당 코드에 대한 이해를 돕는 설명이나 디버깅을 위해 작성한 구문을 의미합니다.
  이러한 주석은 다른 HTML 코드와는 달리 웹 브라우저에 의해 표현되지 않습니다.

```html
<!-- 주석내용 -->
```

### 엔티티**(Entity)**

- HTML에는 미리 예약된 몇몇 문자가 있으며, 이러한 문자를 HTML 예약어(reserved characters)라고 부른다.

```html
&엔티티이름;
또는
&#엔티티숫자;
```

```html
<p></p>
<p>태그는 두 번째로 큰 제목을 나타내는 태그입니다.</p>

<p>&lt;p&gt;태그는 단락을 나타내는 태그입니다.</p>
```

위의 예시처럼 HTML 코드에서 사용된 꺾쇠괄호(<>)는 HTML 태그의 시작과 끝의 의미로 해석됩니다.

> 💡 엔티티(entity)의 이름은 대소문자를 구분합니다.

HTML에서 제공하는 대표적인 엔티티(entity)는 다음과 같습니다.

| 엔티티 문자 | 엔티티 이름 | 16진수 엔티티 숫자 | 설명              |
| ----------- | ----------- | ------------------ | ----------------- |
|             | &nbsp;      | &#160;             | 줄 바꿈 없는 공백 |
| <           | &lt;        | &#60;              | 보다 작은         |
| >           | &gt;        | &#62;              | 보다 큰           |
| &           | &amp;       | &#38;              | AND 기호          |
| "           | &quot;      | &#34;              | 큰따옴표          |
| '           | &apos;      | &#39;              | 작은따옴표        |

- 출처 : [출처](http://www.tcpschool.com/html/html_text_entities)

> 💡 HTML에서 사용할 수 있는 모든 엔티티에 대한 더 자세한 정보에는 W3C 공식 사이트를 방문하여 확인할 수 있다. ( [Character entity references in HTML =>](https://www.w3.org/TR/html4/sgml/entities.html) )

### 문자셋**(Character set)**

- 웹 브라우저가 HTML 문서를 정확하게 나타내기 위해서는 해당 문서가 어떠한 문자셋으로 저장되었는지를 알아야 합니다.
  따라서 HTML 문서가 저장될 때 사용된 문자셋에 대한 정보를 <head>태그 내의 <meta>태그에 명시합니다.

> 💡 HTML5에서 UTF-8의 경우 : <meta charset="UTF-8">

- 위의 두 예시는 해당 HTML 문서가 UTF-8 문자셋을 사용하여 저장되었음을 웹 브라우저에 알려준다.

### 문자셋의 종류

- 현재 사용되는 대표적인 문자셋(character set)은 다음과 같습니다.

1. ASCII : 가장 처음 만들어진 문자셋으로, 인터넷에서 사용할 수 있는 127개의 영문자와 숫자로 이루어져 있습니다.
2. ANSI : 윈도우즈에서 만든 문자셋으로, 총 256개의 문자 코드를 지원합니다.
3. ISO-8859-1 : 256개의 문자 코드를 지원하는 HTML4의 기본 문자셋입니다.
4. UTF-8 : 세상에 있는 거의 모든 문자를 표현할 수 있는 유니코드 문자를 지원하는 HTML5의 기본 문자셋입니다.

---

## HTML 기본 요소

### **HTML 링크(Link)란?**

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

### target 속성

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

### 링크의 상태(state)

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

### HTML 이미지(Image)

- 이미지(image)란 2차원 평면 위에 그려진 시각적 요소를 의미합니다.
  오늘날 웹 페이지에는 이러한 이미지가 매우 중요한 요소의 하나로 자리 잡고 있습니다.
- 웹 페이지에서 주로 사용되는 이미지의 종류는 다음과 같습니다.

- PEG
  [다운로드 (1).jfif](<https://s3-us-west-2.amazonaws.com/secure.notion-static.com/49f3e32b-e634-443e-9871-97a62d5f79c5/%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C_(1).jfif>)
- PNG
  ![PNG 이미지.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/899b8daa-4402-4d28-853f-6be254865c58/PNG_%EC%9D%B4%EB%AF%B8%EC%A7%80.png)
- GIF
  ![gIF 이미지 자료.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/04da91da-183a-4825-9154-5132a3be1764/gIF_%EC%9D%B4%EB%AF%B8%EC%A7%80_%EC%9E%90%EB%A3%8C.gif)

### 이미지의 삽입

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

### 이미지의 크기(width, height) 설정

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

### HTML 리스트(List)

- 리스트(list)란 여러 요소들을 일렬로 나열한 목록이나 명단을 의미합니다.
  - HTML에서는 이러한 리스트를 표현하기 위해 다음과 같은 리스트를 제공하고 있습니다.
  1. 순서가 없는 리스트(unordered list)
  2. 순서가 있는 리스트(ordered list)
  3. 정의 리스트(definition list)

### 순서가 없는 리스트

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
