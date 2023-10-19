# HTML 요소의 타입

## 블록과 인라인

> HTML의 모든 요소는 해당 요소가 웹 브라우저에 어떻게 보이는가를 결정짓는 display 속성을 가집니다. 대부분의 HTML 요소는 이러한 display 속성값으로 다음 두 가지 값 중 하나를 가지게 됩니다.

1. 블록(block)
2. 인라인(inline)

### **블록(block) 타입의 요소**

> display 속성값이 블록(block)인 요소는 언제나 새로운 라인(line)에서 시작하며, 해당 라인의 모든 너비를 차지합니다.

```html
<p style="border: 3px solid red">p요소는 display 속성값이 블록인 요소입니다.</p>
```

> 💡 `<p>` ,`<div>`, `<h>`, `<ul>`, `<ol>`, `<form>`요소는 display 속성값이 블록(block)인 대표적인 요소이다.

---

## < div > 요소

- `<div>`요소는 다른 HTML 요소들을 하나로 묶는 데 자주 사용되는 대표적인 블록(block) 요소입니다.

- `<div>`요소는 주로 여러 요소들의 스타일을 한 번에 적용하기 위해 사용됩니다.

```html
<div style="background-color:lightgrey; color:green; text-align:center">
  <h1>div요소를 이용한 스타일 적용</h1>

  <p>
    이렇게 div요소로 여러 요소들을 묶은 다음에 style 속성과 클래스 등을 이용하여
    한 번에 스타일을 적용할 수 있습니다.
  </p>
</div>
```

### **인라인(inline) 타입의 요소**

- display 속성값이 인라인(inline)인 요소는 새로운 라인(line)에서 시작하지 않습니다.
  또한, 요소의 너비도 해당 라인 전체가 아닌 해당 HTML 요소의 내용(content)만큼만 차지합니다.

```html
<p>
  <span style="background-color:grey; color:orange">span태그</span>는 display
  속성값이 인라인인 요소입니다.
</p>
```

### `<span>` 요소

> `<span>`요소는 텍스트(text)의 특정 부분을 묶는 데 자주 사용되는 인라인(inline) 요소입니다.
>
> `<span>` 요소는 주로 텍스트의 특정 부분에 따로 스타일을 적용하기 위해 사용됩니다.

```html
<p>
  이렇게

  <span style="border: 3px solid red">span요소로 텍스트의 일부분</span>

  만을 따로 묶은 후에 스타일을 적용할 수 있습니다.
</p>
```

---

## **iframe 요소**

- iframe이란 inline frame의 약자입니다.
- iframe 요소를 이용하면 해당 웹 페이지 안에 어떠한 제한 없이 또 다른 하나의 웹 페이지를 삽입할 수 있습니다.

```html
<iframe src="삽입할페이지주소"></iframe>
```

- iframe 요소는 frame 요소와는 달리 종료 태그가 존재합니다.
- 또한, iframe 요소는 명시된 크기로 삽입되는 창의 크기가 고정됩니다.

```html
<iframe src="/css/intro" style="width:100%; height:300px"> </iframe>
```

## 레이아웃

### HTML 레이아웃(Layout)란?

- 레이아웃(layout)이란 특정 공간에 여러 구성 요소를 보기 좋게 효과적으로 배치하는 작업을 의미합니다.
- 웹 페이지의 레이아웃은 웹 사이트의 외관을 결정짓는 매우 중요한 요소입니다.

- HTML에서는 다음과 같은 방법으로 레이아웃을 작성할 수 있습니다.

1. div 요소를 이용한 레이아웃
2. HTML5 레이아웃
3. table 요소를 이용한 레이아웃

### div 요소를 이용한 레이아웃

- div 요소는 CSS 스타일을 손쉽게 적용할 수 있으므로, 레이아웃을 작성하는데 자주 사용됩니다.

```html
<div id="header"><h2>Header 영역</h2></div>

<div id="nav"><h2>Nav 영역</h2></div>

<div id="section"><p>Section 영역</p></div>

<div id="footer"><h2>Footer 영역</h2></div>
```

- 위의 예제에서 사용된 float 속성에 대한 더 자세한 사항은 CSS 플로트에서 확인할 수 있습니다.

### HTML5 레이아웃

- HTML5에서는 웹 페이지의 레이아웃만을 위한 별도의 새로운 요소들을 제공합니다.
  이러한 요소들을 의미(semantic) 요소라고 합니다.
  ![Untitled](https://www.tcpschool.com/lectures/img_html_html5_layout.png)

  ```html
  <header><h2>Header 영역</h2></header>

  <nav><h2>Nav 영역</h2></nav>

  <section><p>Section 영역</p></section>

  <footer><h2>Footer 영역</h2></footer>
  ```

  - HTML5에서 제공하는 레이아웃만을 위한 의미(semantic) 요소는 다음과 같습니다.
    | 의미 요소 | 설명 |
    | --------- | ------------------------------------------------------------ |
    | `<header>` | HTML 문서나 섹션(section) 부분에 대한 헤더(header)를 정의함. |
    | `<nav>` | HTML 문서의 탐색 링크를 정의함. |
    | `<section>` | HTML 문서에서 섹션(section) 부분을 정의함. |
    | `<article>` | HTML 문서에서 독립적인 하나의 글(article) 부분을 정의함. |
    | `<aside>` | HTML 문서에서 페이지 부분 이외의 콘텐츠(content)를 정의함. |
    | `<footer>` | HTML 문서나 섹션(section) 부분에 대한 푸터(footer)를 정의함. |
  - HTML5에서 새로 소개된 의미 요소에 대한 더 자세한 사항은 HTML5 의미 요소에서 확인할 수 있습니다.

### table 요소를 이용한 레이아웃

- table 요소를 이용하여 레이아웃을 작성하는 방법은 오래전에 사용하던 방식이며, 현재는 거의 사용하지 않습니다.
- table 요소는 레이아웃을 만들기 위해 설계된 요소가 아니므로, 테이블로 작성된 레이아웃은 수정이 매우 힘듭니다.

```html
<table width="100%" style="text-align:center; border:none">
  <tr>
    <td colspan="2" style="background-color:lightgrey"><h2>Header 영역</h2></td>
  </tr>

  <tr>
    <td style="background-color:#339999; color:white; width:20%">
      <h2>Nav 영역</h2>
    </td>

    <td style="height:200px; text-align:left"><p>Section 영역</p></td>
  </tr>

  <tr>
    <td colspan="2" style="background-color:#FFCC00"><h2>Footer 영역</h2></td>
  </tr>
</table>
```

> 💡 따라서 되도록이면 table 요소로 레이아웃을 작성하지 말아야 합니다.

---
