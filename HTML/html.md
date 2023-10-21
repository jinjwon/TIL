# HTML

![HTML](https://reference.uz/wp-content/uploads/2019/04/html5-1024x576.jpg)

## HTML이란?

- **HTML은 HyperText Markup Language의 약자입니다.**
  **웹 페이지는 HTML 문서라고도 불리며, HTML 태그들로 구성됩니다.**
  **각각의 HTML 태그는 웹 페이지의 디자인이나 기능을 결정하는데 사용됩니다.**

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

### 주석

- 주석(comment)이란 개발자가 작성한 해당 코드에 대한 이해를 돕는 설명이나 디버깅을 위해 작성한 구문을 의미합니다.
  이러한 주석은 다른 HTML 코드와는 달리 웹 브라우저에 의해 표현되지 않습니다.

```html
<!-- 주석내용 -->
```

---

## **HTML 스타일(Style)**

- HTML 요소의 style 속성(attribute)을 이용하면 CSS 스타일을 HTML 요소에 직접 설정할 수 있습니다.
  하지만 이러한 style 속성을 이용한 방법은 오직 단 하나의 HTML 요소에만 스타일을 적용할 수 있습니다.

```html
<태그이름 style="속성이름:속성값">
```

### 여러 스타일의 설정

- style 속성을 이용하여 여러 CSS 스타일을 한 번에 적용할 수 있습니다.

```html
<h1
  style="background-color:white; color:maroon; font-size:150%; text-align:center"
>
  style 속성을 이용하여 한 번에 스타일링 하기!
</h1>
```

> 💡 style 속성값에 사용되는 CSS 속성(property)과 속성값들은 세미콜론(;)을 이용하여 구분합니다.
> 💡 CSS 속성을 하나만 사용할 때나, 여러 개의 CSS 속성 중 맨 마지막 CSS 속성은 세미콜론(;)을 생략할 수 있습니다.

---
