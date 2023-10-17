# CSS

![CSS](https://colorlib.com/wp/wp-content/uploads/sites/2/creative-css3-tutorials.jpg)

## CSS이란?

> CSS는 Cascading Style Sheets의 약자입니다.
>
> CSS는 HTML 요소들이 각종 미디어에서 어떻게 보이는가를 정의하는 데 사용되는 스타일 시트 언어입니다.
>
> HTML4 부터는 이러한 모든 서식 설정을 HTML 문서로부터 따로 분리하는 것이 가능해졌습니다.
>
> 오늘날 대부분의 웹 브라우저들은 모두 CSS를 지원하고 있습니다

## CSS 문법

![css 문법](https://www.tcpschool.com/lectures/img_css_syntax.png)

### CSS 선택자

- HTML 요소 선택자
- 아이디(id) 선택자
- 클래스(class) 선택자
- 그룹(group) 선택자

#### HTML 요소 선택자

```<style>

        h2 { color: teal; text-decoration: underline; }

    </style>

    ...

    <h2>이 부분에 스타일을 적용합니다.</h2>
```

### 아이디(id) 선택자

- 아이디 선택자는 CSS를 적용할 대상으로 특정 요소를 선택할 때 사용합니다.
- 이 선택자는 웹 페이지에 포함된 여러 요소 중에서 특정 아이디 이름을 가지는 요소만을 선택해 줍니다.

```<style>

    #heading { color: teal; text-decoration: line-through; }

</style>

...

<h2 id="heading">이 부분에 스타일을 적용합니다.</h2>
```

**💡 이렇게 중복된 아이디를 가지고 자바스크립트 작업을 하게 되면 오류가 발생합니다.**
**따라서 되도록이면 하나의 웹 페이지에 속하는 요소에는 다른 아이디 이름을 사용하거나클래스를 사용하는 것이 좋습니다.**

---

### 클래스(class) 선택자

- 클래스 선택자는 특정 집단의 여러 요소를 한 번에 선택할 때 사용합니다.
  이러한 특정 집단을 클래스(class)라고 하며, 같은 클래스 이름을 가지는 요소들을 모두 선택해 줍니다.

```html
<style>
  .headings {
    color: lime;
    text-decoration: overline;
  }
</style>

...

<h2 class="headings">이 부분에 스타일을 적용합니다.</h2>

<p>
  class 선택자를 이용하여 스타일을 적용할 HTML 요소들을 한 번에 선택할 수
  있습니다.
</p>

<h3 class="headings">이 부분에도 같은 스타일을 적용합니다.</h3>
```

### 그룹(group) 선택자

- 그룹 선택자는 위에서 언급한 여러 선택자를 같이 사용하고자 할 때 사용합니다.
- 그룹 선택자는 여러 선택자를 쉼표(,)로 구분하여 연결합니다.
- 이러한 그룹 선택자는 코드를 중복해서 작성하지 않도록 하여 코드를 간결하게 만들어 줍니다.

  ```html
  <style>
    h1 {
      color: navy;
    }

    h1,
    h2 {
      text-align: center;
    }

    h1,
    h2,
    p {
      background-color: lightgray;
    }
  </style>
  ```

### **CSS 주석(comments)**

- 주석(comment)이란 개발자가 작성한 해당 코드에 대한 이해를 돕는 설명이나 디버깅을 위해 작성한 구문을 의미합니다.
- 이러한 주석은 다른 CSS 코드와는 달리 웹 브라우저에 의해 해석되지 않습니다.

  ```html
  /* 주석내용 */
  ```

- 다음 예제는 첫 번째 주석 안에 한 줄짜리 두 번째 주석을 삽입한 예제입니다.
  이때 첫 번째 주석의 두 번째 라인은 두 번째 주석의 \*/ 기호로 인해 정상적인 주석으로 인식되지 못합니다.

```html
/* 첫 번째 주석의 첫 번째 라인입니다. /* 두 번째 주석입니다. */ 첫 번째 주석의
두 번째 라인입니다. */
```

---

## CSS 색

- CSS에서 색을 표현하는 방법에는 다음과 같이 세 가지 방법이 있습니다.

1. 색상 이름으로 표현
2. RGB 색상값으로 표현
3. 16진수 색상값으로 표현

### **색상 이름으로 표현**

- W3C에서 정의한 16개의 HTML4 표준 색상 이름은 다음과 같다.

![CSS color](https://make.wordpress.org/core/files/2021/02/wordpress-admin-color-palette-WP57.png)

> 💡 HTML에서 색상 이름은 대소문자를 구분하지 않습니다.

**_예시_**

```html
<style>
  .blue {
    color: blue;
  }

  .green {
    color: green;
  }

  .silver {
    color: silver;
  }
</style>
```

- 현재는 대부분의 브라우저가 140개의 색상 이름을 지원하고 있다.

### RGB 색상값으로 표현

- 모니터나 스크린은 빨간색(Red), 녹색(Green), 파란색(Blue)을 혼합하여 색을 표현합니다. 따라서 HTML에서도 이 세 가지 색을 가지고 색을 표현하는 RGB 색상을 사용합니다.

- RGB 색상의 기본색(Red, Green, Blue)은 각각 0부터 255까지의 범위를 가집니다.

**_예시_**

```html
<style>
  .blue {
    color: rgb(0, 0, 255);
  }

  .green {
    color: rgb(0, 128, 0);
  }

  .silver {
    color: rgb(192, 192, 192);
  }
</style>
```

### 16진수 색상값으로 표현

- 16진수 색상값은 RGB 색상값을 각각 16진수로 변환한 것입니다.
  따라서 RGB 색상의 기본색(Red, Green, Blue)은 각각 00부터 FF까지의 범위를 가집니다.

- 예를 들면, 녹색을 나타내는 RGB 색상값 rgb(0,255,0)은 16진수 색상값으로는 #00FF00이 됩니다.

**_예시_**

```html
<style>
  .blue {
    color: #0000ff;
  }

  .green {
    color: #008000;
  }

  .silver {
    color: #c0c0c0;
  }
</style>
```

---

## CSS 배경

- 웹 페이지뿐만 아니라 HTML 요소는 모두 각자의 배경을 가지고 있습니다.
  CSS의 background 속성은 이러한 각 요소의 배경에 다양한 효과를 줄 수 있게 해줍니다.

- CSS에서 사용할 수 있는 background 속성은 다음과 같습니다.

1. background-color
2. background-image
3. background-repeat
4. background-position
5. background-attachment

### **background-color 속성**

- background-color 속성은 해당 HTML 요소의 배경색(background color)을 설정합니다.

```html
<style>
  body {
    background-color: lightblue;
  }

  h1 {
    background-color: rgb(255, 128, 0);
  }

  p {
    background-color: #ffffcc;
  }
</style>
```

### **background-image 속성**

- background-image 속성은 해당 HTML 요소의 배경으로 나타날 배경 이미지(image)를 설정합니다. 설정된 배경 이미지는 기본 설정으로 HTML 요소 전체에 걸쳐 반복되어 나타납니다.

```html
<style>
  body {
    background-image: url("/examples/images/img_background_good.png");
  }
</style>
```

**_예시_**

```html
<style>
  body {
    background-image: url("/examples/images/img_background_bad.png");
  }
</style>
```

- 배경 이미지를 사용할 때에는 이미지가 본문의 텍스트를 방해하지 않도록 주의를 기울여야 합니다.

### **background-position 속성**

- background-position 속성은 반복되지 않는 배경 이미지의 상대 위치(relative position)를 설정합니다.

**_예시_**

```html
<style>
  body {
    background-image: url("/examples/images/img_man.png");

    background-repeat: no-repeat;

    background-position: top right;
  }
</style>
```

- 이 속성에서 사용할 수 있는 키워드의 조합은 다음과 같다.

1. left top
2. left center
3. left bottom
4. right top
5. right center
6. right bottom
7. center top
8. center center
9. center bottom

- 또한, 퍼센트(%)나 픽셀(px)을 사용하여 상대 위치를 직접 명시할 수도 있습니다. 이때 상대 위치를 결정하는 기준은 해당 요소의 왼쪽 상단(left top)이 됩니다.

- 다음 예시는 배경 이미지의 상대 위치를 픽셀 단위로 직접 명시한 예시입니다.

```html
<style>
  body {
    background-image: url("/examples/images/img_man.png");

    background-repeat: no-repeat;

    background-position: 100px 200px;
  }
</style>
```

### background-attachment 속성

- background-attachment 속성을 사용하여 위치가 설정된 배경 이미지를 해당 위치에 고정시킬 수도 있습니다.
- 이렇게 고정된 배경 이미지는 스크롤과는 무관하게 화면의 위치에서 이동하지 않습니다.

  ```css
  <style>

      body {

          background-image: url("/examples/images/img_man.png");

          background-repeat: no-repeat;

          background-position: left bottom;

          background-attachment: fixed;

      }

  </style>
  ```

### background 속성 한 번에 적용하기

- 위에서 언급한 모든 background 속성을 이용한 스타일을 한 줄에 설정할 수 있습니다.

  ```css
  <style>

      body { background: #FFCCCC url("/examples/images/img_man.png") no-repeat left bottom fixed; }

  </style>
  ```

### **CSS background 속성**

| 속성                  | 설명                                                           |
| --------------------- | -------------------------------------------------------------- |
| background            | 모든 background 속성을 이용한 스타일을 한 줄에 설정할 수 있음. |
| background-color      | HTML 요소의 배경색을 설정함.                                   |
| background-image      | HTML 요소의 배경 이미지를 설정함.                              |
| background-repeat     | 설정된 배경 이미지의 반복 유무를 설정함.                       |
| background-position   | 반복되지 않는 배경 이미지의 상대 위치를 설정함.                |
| background-attachment | 배경 이미지를 스크롤과는 무관하게 해당 위치에 고정시킴.        |

---

## CSS 텍스트

- CSS는 여러 기능을 가진 다양한 Text 속성을 제공합니다.

- CSS에서 사용할 수 있는 대표적인 text 속성은 다음과 같습니다.

1. color
2. direction
3. letter-spacing
4. word-spacing
5. text-indent
6. text-align
7. text-decoration
8. text-transform
9. line-height
10. text-shadow

### color속성

- color 속성은 텍스트의 색상을 설정합니다.
- 웹 페이지에서 텍스트의 기본 색상은 검정색입니다.
  `<body>`태그에 명시된 color 속성값은 웹 페이지 내의 모든 텍스트 요소에 적용됩니다.
  하지만 각 요소별로 따로 명시된 color 속성값이 있다면, 해당 속성값이 `<body>`태그에 명시된 속성값보다 우선 적용됩니다.

```html
<style>
  body {
    color: red;
  }

  p {
    color: maroon;
  }
</style>
```

### **direction 속성**

- direction 속성은 텍스트가 써지는 방향을 설정합니다.
- 웹 페이지에서 텍스트는 기본적으로 왼쪽에서 오른쪽 방향으로 써집니다.
  direction 속성이 left-to-right(ltr)일 때는 기본 설정처럼 텍스트가 왼쪽에서 오른쪽 방향으로 써집니다.
  하지만, direction 속성이 right-to-left(rtl)일 때는 텍스트가 반대 방향인 오른쪽에서 왼쪽 방향으로 써집니다.
- 다음 예시는 "객체 지향 프로그래밍"이라는 문자열을 한글과 아랍어로 각각 나타낸 예시다.

```html
<style>
  .rightToLeft {
    direction: rtl;
  }
</style>
```

- 아랍어는 한글이나 영어와는 달리 오른쪽에서 왼쪽 방향으로 텍스트를 읽고 쓰는 언어입니다.
- 따라서 아랍어와 같이 텍스트를 반대 방향으로 쓰는 언어를 나타낼 때는 텍스트가 써지는 방향을 direction 속성을 사용하여 변경해 줘야 합니다.

### **letter-spacing 속성**

- letter-spacing 속성은 텍스트 내에서 글자 사이의 간격을 설정합니다

```html
<style>
  .decLetterSpacing {
    letter-spacing: -3px;
  }

  .incLetterSpacing {
    letter-spacing: 10px;
  }
</style>
```

### **word-spacing 속성**

- word-spacing 속성은 텍스트 내에서 단어 사이의 간격을 설정합니다.
- letter-spacing 속성과는 달리 문자 간의 간격이 아닌 단어 간의 간격을 기준으로 설정합니다

```html
<style>
  .decWordSpacing {
    word-spacing: -3px;
  }

  .incWordSpacing {
    word-spacing: 10px;
  }
</style>
```

### **text-indent 속성**

- text-indent 속성은 단락의 첫 줄에 들여쓰기할지 안 할지를 설정합니다.
  웹 페이지에서 단락은 기본적으로 들여쓰기가 설정되어 있지 않습니다.

```html
<style>
  .paraIndent {
    text-indent: 30px;
  }
</style>
```

### text-align 속성

- text-align 속성은 텍스트의 수평 방향 정렬을 설정합니다.
  text-align 속성으로 설정된 정렬 방향은 text-direction 속성과는 상관없이 우선적으로 적용됩니다

  ```html
  .<style>
    h2 {
      text-align: left;
    }

    h3 {
      text-align: right;
    }

    h4 {
      text-align: center;
    }
  </style>
  ```

### text-decoration 속성

- text-decoration 속성은 텍스트에 여러 가지 효과를 설정하거나 제거하는데 사용합니다.

  ```html
  <style>
    h2 {
      text-decoration: overline;
    }

    h3 {
      text-decoration: line-through;
    }

    h4 {
      text-decoration: underline;
    }

    a {
      text-decoration: none;
    }
  </style>
  ```

> 💡 text-decoration 속성값을 none으로 설정하여 링크(link)가 설정된 텍스트의 밑줄을 제거하는데 자주 사용합니다.

### text-transform 속성

> text-transform 속성은 텍스트에 포함된 영문자에 대한 대소문자를 설정합니다.
>
> 이 속성은 텍스트에 포함된 모든 영문자를 대문자나 소문자로 변경시켜 줍니다.
>
> 또한, 단어의 첫 문자만을 대문자로 변경시킬 수도 있습니다.

```html
<style>
  h2 {
    text-transform: uppercase;
  }
  h3 {
    text-transform: lowercase;
  }
  h4 {
    text-transform: capitalize;
  }
</style>
```

> 💡 text-transform 속성은 한글에는 영향을 주지 않으며, 오직 영문자에만 적용됩니다.

### line-height 속성

- line-height 속성은 텍스트의 줄 간격을 설정합니다.

  ```html
  <style>
    .narrowLineHeight {
      line-height: 0.8;
    }
    .wideLineHeight {
      line-height: 1.8;
    }
  </style>
  ```

### text-shadow 속성

- text-shadow 속성은 텍스트에 간단한 그림자 효과를 설정합니다.

  ```html
  <style>
    h2  {
       text-shadow: * * 2px * *   * * 1px * *   * * #3399cc * *;
    }
  </style>
  ```

## **CSS text 속성**

| 속성            | 설명                                                             |
| --------------- | ---------------------------------------------------------------- |
| color           | 텍스트의 색상을 설정함.                                          |
| direction       | 텍스트가 쓰이는 방향을 설정함.                                   |
| letter-spacing  | 텍스트 내에서 문자 사이의 간격을 설정함.                         |
| word-spacing    | 텍스트 내에서 단어 사이의 간격을 설정함.                         |
| text-indent     | 단락의 첫 줄을 들여쓰기할지 안 할지를 설정함.                    |
| text-align      | 텍스트의 수평 방향 정렬을 설정함.                                |
| text-decoration | 텍스트에 여러 가지 효과를 설정하거나 제거함.                     |
| text-transform  | 텍스트에 포함된 영문자에 대한 대소문자를 설정함.                 |
| line-height     | 텍스트의 줄 간격을 설정함.                                       |
| text-shadow     | 텍스트에 그림자 효과를 설정함.                                   |
| unicode-bidi    | direction 속성과 같이 사용하여 텍스트의 기본 출력 방향을 설정함. |
| vertical-align  | HTML 요소 내의 수직 방향 정렬을 설정함.                          |
| white-space     | HTML 요소 내의 여백을 설정함.                                    |

---

## CSS 글꼴

- CSS에서 사용할 수 있는 font 속성은 다음과 같습니다.
  1. font-family
  2. font-style
  3. font-variant
  4. font-weight
  5. font-size

### CSS 글꼴 집합(font-family)

- CSS에는 두 가지의 글꼴 집합(font family)이 존재합니다.
  - font family : 특정 글꼴 집합 ("Times", "Courier" 등)
  - generic family : 비슷한 모양을 가지는 글꼴 집합 ("Serif", "Monospace" 등)

### font-family 속성

- font-family 속성은 하나의 글꼴만을 설정할 수도 있고, 여러 개의 글꼴을 같이 설정할 수도 있습니다.
  font-family 속성값이 여러 개의 글꼴로 설정되어 있으면, 웹 브라우저는 위에서부터 순서대로 글꼴을 읽어 들입니다.

  만약 사용자의 컴퓨터에 첫 번째로 읽어 들인 글꼴이 없으면 다음 글꼴을 확인하게 됩니다.

  이런 방식으로 계속해서 읽어 들인 글꼴이 존재하는지를 확인하여, 읽어 들인 글꼴이 사용자의 컴퓨터에 존재하면 해당 글꼴로 표시하게 됩니다.

  글꼴의 이름이 한 단어 이상으로 이루어지면 반드시 따옴표를 사용하여 둘러 쌓아야 합니다.
  또한, 여러 개의 글꼴을 나열할 때에는 쉼표(,)로 구분 짓습니다.

```html
<style>
  .serif {
    font-family: "Times New Roman", Times, serif;
  }

  .sansserif {
    font-family: Arial, Helvetica, sans-serif;
  }
</style>
```

### font-style 속성

font-style 속성은 주로 이탤릭체를 사용하기 위해 사용하며, 다음과 같이 3가지의 속성값을 가집니다.

- normal : 텍스트에 어떠한 스타일도 적용하지 않습니다.
- italic : 텍스트를 이탤릭체로 나타냅니다.
- oblique : 텍스트를 기울입니다. 이 속성값은 italic과 매우 유사하지만 지원하는 웹 브라우저가 거의 없습니다.

  ```html
  <style>
    .normal {
      font-style: normal;
    }

    .italic {
      font-style: italic;
    }

    .oblique {
      font-style: oblique;
    }
  </style>
  ```

### font-variant 속성

- font-variant 속성은 속성값이 small-caps로 설정되면, 텍스트에 포함된 영문자 중 모든 소문자를 작은 대문자(small-caps) 글꼴로 변경시킵니다.
- 이때 영문자 중 대문자는 기존 크기 그대로 출력합니다.
- 작은 대문자(small-caps) 글꼴이란 텍스트의 기존 대문자보다는 약간 작은 크기의 대문자를 의미합니다.

  ```html
  <style>
    .normal {
      font-variant: normal;
    }

    .smallCaps {
      font-variant: small-caps;
    }
  </style>
  ```

  > 💡 font-variant 속성은 한글에는 적용되지 않으며, 영문자에만 적용됩니다.

### font-weight 속성

- font-weight 속성은 텍스트를 얼마나 두껍게 표현할지를 설정합니다.

  - 사용할 수 있는 속성값에는 lighter, normal, bold, bolder 등이 있습니다.
  - 또한, 100, 200, 300, ... , 900 등과 같이 숫자로 텍스트의 두께를 설정할 수도 있습니다.

  ```html
  <style>
    .normal {
      font-weight: normal;
    }

    .bold {
      font-weight: 600;
    }

    .bolder {
      font-weight: bolder;
    }
  </style>
  ```

### font-size 속성

- font-size 속성은 텍스트의 크기를 설정합니다.

- 웹 디자인에서 텍스트의 크기는 매우 중요한 표현 요소입니다.
  - 하지만 제목을 표현하기 위해서 텍스트의 크기만을 크게 해서는 안 됩니다.
  - 이때에는 제목을 위한 HTML 요소인 `<h1>`태그부터 `<h6>`태그를 사용해야 합니다.

### font-size 속성값

- font-size 속성값은 다음과 같이 두 가지 방식으로 표현할 수 있습니다.

1. 절대적 크기
2. 상대적 크기

- 절대적 크기는 텍스트의 크기를 명시된 크기 그대로 설정하고자 할 때 사용합니다.

  절대적 크기로 설정된 텍스트는 모든 웹 브라우저에서 같은 크기로 표현됩니다.

- 상대적 크기는 텍스트를 둘러싸고 있는 HTML 요소들의 크기에 따라 텍스트의 크기도 같이 변하는 방식입니다.
  또한, 사용자가 웹 브라우저를 통해 텍스트의 크기를 직접 변경할 수도 있습니다.

### font-size의 크기 단위

- font-size 속성값에 자주 사용되는 대표적인 크기 단위는 다음과 같습니다.
- 백분율 단위(%)는 기본 크기를 100%로 놓고, 그에 대한 상대적인 크기를 설정합니다.
- 배수 단위(em)는 해당 글꼴(font)의 기본 크기를 1em으로 놓고, 그에 대한 상대적인 크기를 설정합니다.
- 픽셀 단위(px)는 스크린의 픽셀(pixel)을 기준으로 하는 절대적인 크기를 설정합니다.

  ```html
  <style>
    body {
      font-size: 100%;
    }

    #large {
      font-size: 2.5em;
    }

    #small {
      font-size: 0.7em;
    }

    #fixed {
      font-size: 20px;
    }
  </style>
  ```

  > 💡 배수 단위(em)로 설정된 텍스트는 사용자가 웹 브라우저를 통해 크기를 재조정할 수 있습니다.

### **CSS font 속성**

| 속성         | 설명                                                                          |
| ------------ | ----------------------------------------------------------------------------- |
| font         | 모든 font 속성을 이용한 스타일을 한 줄에 설정할 수 있음.                      |
| font-family  | 텍스트의 글꼴 집합(font family)을 설정함.                                     |
| font-style   | 주로 이탤릭체를 사용하기 위해 사용함.                                         |
| font-variant | 텍스트에 포함된 영문자 중 소문자만을 작은 대문자(small-caps) 글꼴로 변경시킴. |
| font-weight  | 텍스트를 얼마나 두껍게 표현할지를 설정함.                                     |
| font-size    | 텍스트의 크기를 설정함.                                                       |

---

## CSS 링크

- 링크(link)에는 color, font-family, background 속성 등 CSS의 다양한 속성들을 적용할 수 있습니다.

  - 또한, text-decoration 속성값을 none으로 설정하여, 링크가 연결된 텍스트의 밑줄을 제거할 수도 있습니다.

    ```html
    <style>
      a {
        background-color: #ffffe0;

        color: darkslategray;

        font-size: 1.3em;

        text-decoration: none;
      }
    </style>
    ```

### 링크(link)의 상태

- 링크는 총 5가지의 상태를 가지며, 각 상태마다 다른 스타일을 적용할 수 있습니다.

  1. link : 링크의 기본 상태이며, 사용자가 아직 한 번도 해당 링크를 통해 연결된 페이지를 방문하지 않은 상태입니다.
  2. visited : 사용자가 한 번이라도 해당 링크를 통해 연결된 페이지를 방문한 상태입니다.
  3. hover : 사용자의 마우스 커서가 링크 위에 올라가 있는 상태입니다.
  4. active : 사용자가 마우스로 링크를 클릭하고 있는 상태입니다.
  5. focus : 키보드나 마우스의 이벤트(event) 또는 다른 형태로 해당 요소가 포커스(focus)를 가지고 있는 상태입니다.

     ```html
     <style>
       a:link {
         color: olive;
       }

       a:visited {
         color: brown;
       }

       a:hover {
         color: coral;
       }

       a:active {
         color: khaki;
       }
     </style>
     ```

### 링크를 활용한 버튼(Button)

- CSS를 이용하면 간단하게 링크를 버튼처럼 만들 수 있습니다.

  ```html
  <style>
    a:link,
    a:visited {
      background-color: #ffa500;

      color: maroon;

      padding: 15px 25px;

      text-align: center;

      text-decoration: none;

      display: inline-block;
    }

    a:hover,
    a:active {
      background-color: #ff4500;
    }
  </style>
  ```

---

## CSS 리스트

- CSS에서 사용할 수 있는 list-style 속성은 다음과 같습니다.
  1. list-style-type
  2. list-style-image
  3. list-style-position

### list-style-type 속성

- 리스트 요소의 앞에 위치하는 숫자나 기호를 마커(marker)라고 합니다.
  list-style-type 속성을 이용하면 리스트에 다양한 마커(marker)를 적용할 수 있습니다.

  ```html
  <style>
    .circle {
      list-style-type: circle;
    }

    .square {
      list-style-type: square;
    }

    .upperAlpha {
      list-style-type: upper-alpha;
    }

    .lowerRoman {
      list-style-type: lower-roman;
    }
  </style>
  ```

  - 사용할 수 있는 마커(marker)에 대한 더 자세한 사항은 HTML 리스트에서 확인할 수 있습니다.

### list-style-image 속성

- list-style-image 속성을 이용하면 마커(marker)로 자신만의 이미지를 사용할 수 있습니다.

  ```html
  <style>
    .imageMarker {
      list-style-image: url("/examples/images/img_list_marker.png");
    }
  </style>
  ```

### list-style-position 속성

- list-style-position 속성을 이용하면 리스트 요소의 위치를 설정할 수 있습니다.

  - list-style-position 속성의 기본 속성값은 outside로 설정되어 있습니다.

  ```html
  <style>
    .outside {
      list-style-position: outside;
    }

    .inside {
      list-style-position: inside;
    }
  </style>
  ```

### list-style 속성 한 번에 적용하기

- 위에서 언급한 모든 list-style 속성을 이용한 스타일을 한 줄에 설정할 수 있습니다.

  ```html
  <style>
    ul {
      list-style: square inside url("/examples/images/img_list_marker.png");
    }
  </style>
  ```

### 리스트에 배경색 적용

- CSS를 사용하면 리스트 전체뿐만 아니라 리스트 요소별로도 각각의 배경색을 설정할 수 있습니다.

  ```html
  <style>

      ul { background: #D2691E; padding: 15px; }

      ol { background: #6495ED; padding: 15px; }

      ul li { background: #DEB887; margin: 5px; }

      ol li { background: #00FFFF; margin-left: 15px; }

  ```

### **CSS list-style 속성**

| 속성                | 설명                                                           |
| ------------------- | -------------------------------------------------------------- |
| list-style          | 모든 list-style 속성을 이용한 스타일을 한 줄에 설정할 수 있음. |
| list-style-type     | 리스트 요소의 마커(marker)를 설정함.                           |
| list-style-image    | 리스트 요소의 마커로 사용할 이미지를 설정함.                   |
| list-style-position | 리스트 요소의 위치를 설정함.                                   |

---

## CSS 테이블

- 테이블에 다음 속성을 사용하여 CSS 스타일을 적용할 수 있습니다.
  1. border
  2. border-collapse
  3. border-spacing
  4. caption-side
  5. empty-cells
  6. table-layout

### border 속성

- border 속성으로 테이블의 테두리(border)를 설정할 수 있습니다.
  이 속성을 명시하지 않으면 해당 테이블은 기본 설정으로 빈 테두리를 가지게 됩니다.

  ```html
  <style>
    table,
    th,
    td {
      border: 2px solid orange;
    }
  </style>
  ```

- 위의 예제에서 테이블의 테두리(border)가 두 줄씩 나타나는 이유는 `<th>`태그와 `<td>`태그가 각각 자신만의 테두리를 가지고 있기 때문입니다.
- 위와 같이 두 줄로 표현되는 테두리를 한 줄로 설정하려면 border-collapse 속성을 사용해야 합니다.

### border-collapse 속성

- border-collapse 속성값을 collapse로 설정하면 해당 테이블의 테두리는 한 줄로 표현됩니다.

  - 이 속성을 명시하지 않으면 해당 테이블은 기본 설정으로 테이블 요소별 테두리를 모두 표현하게 됩니다

  ```html
  <style>
    table,
    th,
    td {
      border: 2px solid orange;
    }

    table {
      border-collapse: collapse;
    }
  </style>
  ```

### border-spacing 속성

- border-spacing 속성은 테이블 요소(th, td)간의 여백을 설정해 줍니다.

  ```html
  <style>
    table,
    th,
    td {
      border: 1px solid black;
    }

    table {
      width: 100%;
      border-collapse: seperate;
      border-spacing: 20px 30px;
    }
  </style>
  ```

### text-align 속성

- text-align 속성은 테이블 요소(th, td) 내부에서 텍스트의 수평 방향 정렬을 설정합니다.

  `<th>`태그 내부는 가운데 정렬이, `<td>`태그 내부는 왼쪽 정렬이 기본 설정입니다.

  ```html
  <style>
    table,
    th,
    td {
      border: 1px solid black;
    }

    table {
      border-collapse: collapse;
      width: 100%;
    }

    th {
      text-align: left;
    }

    td {
      text-align: center;
    }
  </style>
  ```

### vertical-align 속성

- vertical-align 속성은 테이블 요소(th, td) 내부에서 텍스트의 수직 방향 정렬을 설정합니다.
- `<th>`태그와 `<td>`태그 모두 가운데 정렬이 기본 설정입니다.

  ```html
  <style>
    table,
    th,
    td {
      border: 1px solid black;
    }

    table {
      border-collapse: collapse;
      width: 100%;
    }

    th {
      vertical-align: top;
      height: 50px;
    }

    td {
      vertical-align: bottom;
      height: 50px;
    }
  </style>
  ```

### 다양한 형태의 테이블 예제

- CSS를 이용하면 HTML 기본 테이블을 훨씬 더 다양한 모습으로 설정할 수 있습니다.
- 다음 예제는 `<th>`태그와 `<td>`태그에 border-bottom 속성을 사용하여 수평 나눔선만으로 만든 테이블입니다.

```html
<style>
  table {
    border-collapse: collapse;
    width: 100%;
  }

  th,
  td {
    padding: 10px;
    border-bottom: 1px solid #cd5c5c;
  }
</style>
```

- 다음 예제는 :hover 선택자를 이용하여 `<tr>`태그에 마우스를 올리면 행 전체가 하이라이트 되도록 만든 테이블입니다.

```html
<style>
  table {
    border-collapse: collapse;
    width: 100%;
  }

  th,
  td {
    padding: 10px;
    border-bottom: 1px solid #cd5c5c;
  }

  tr:hover {
    background-color: #f5f5f5;
  }
</style>
```

- :hover 선택자에 대한 더 자세한 사항은 CSS 동적 의사 클래스에서 확인할 수 있습니다.
- 다음 예제는 background-color 속성과 :nth-child 선택자를 사용하여 얼룩무늬 효과를 설정한 테이블입니다.

```html
<style>
  table {
    border-collapse: collapse;
    width: 100%;
  }

  th,
  td {
    padding: 10px;
  }

  tr:nth-child(odd) {
    background-color: #f3f3f3;
  }
</style>
```

- :nth-child 선택자에 대한 더 자세한 사항은 CSS 구조 의사 클래스에서 확인할 수 있습니다.

### **CSS table 속성**

| 속성            | 설명                                                                      |
| --------------- | ------------------------------------------------------------------------- |
| border          | 모든 border 속성을 이용한 스타일을 한 줄에 설정할 수 있음.                |
| border-collapse | 테이블의 테두리를 한 줄로 나타낼지를 설정함.                              |
| border-spacing  | 테이블 요소(th, td)간의 여백을 설정함.                                    |
| caption-side    | 테이블의 캡션(caption)을 설정함.                                          |
| empty-cells     | 테이블 내의 빈 셀(cell)들의 테두리 및 배경색을 표현할지 안 할지를 설정함. |
| table-layout    | 테이블에 사용되는 레이아웃 알고리즘을 설정함.                             |

---

## CSS 박스 모델

## 크기 단위

- CSS에서 사용하는 크기의 단위에는 %, em, px, cm, mm, inch 등이 있습니다.

- 그 중에서도 가장 많이 쓰이는 크기 단위는 다음과 같습니다.

1. 백분율 단위(%)
2. 배수 단위(em)
3. 픽셀 단위(px)

- 백분율 단위(%)는 기본 크기를 100%로 놓고, 그에 대한 상대적인 크기를 설정합니다.
  배수 단위(em)는 해당 글꼴(font)의 기본 크기를 1em으로 놓고, 그에 대한 상대적인 크기를 설정합니다.
  픽셀 단위(px)는 스크린의 픽셀(pixel)을 기준으로 하는 절대적인 크기를 설정합니다.

```css
<style>

    #large { font-size: 200%; }

    #small { font-size: 0.7em; }

    #fixed { font-size: 20px; }

</style>
```

> 💡 1배 = 1em = 100%를 의미합니다.

---

## CSS 크기

### 크기(Dimension)란?

- CSS를 이용하면 HTML 요소의 크기를 마음대로 설정할 수 있습니다.
- CSS에서 크기 조절을 위해 사용할 수 있는 속성은 다음과 같습니다.
  1. height
  2. width
  3. max-width
  4. min-width
  5. max-height
  6. min-height

---

### height와 width 속성

- height와 width 속성은 HTML 요소의 높이와 너비를 각각 설정합니다.
- 이 속성의 기본 설정값은 auto이며, 웹 브라우저가 각 HTML 요소에 맞게 자동으로 높이와 너비를 설정해 줍니다.

  ```css
  <style>

      div { height: 200px; width: 500px; }

  </style>
  ```

### max-width 속성

> max-width 속성은 해당 HTML 요소가 가질 수 있는 최대 너비(width)를 설정합니다.
>
> - 이 속성의 기본 설정값은 none이며, 해당 HTML 요소의 너비에 제한을 두지 않겠다는 의미입니다.
> - width 속성으로 너비를 설정하면, 설정된 너비 이하로 브라우저의 크기가 줄어들 때 해당 요소에 스크롤 바를 생성하게 됩니다.
> - 하지만 max-width 속성으로 너비를 설정하면 다음과 같이 좀 더 유연한 결과를 얻을 수 있습니다.
> - max-width 속성으로 너비를 설정하면 줄어드는 웹 브라우저의 크기에 맞춰 해당 HTML 요소의 너비도 자동으로 줄어듭니다.

```html
<style>
  div.maxWidth {
    max-width: 500px;
  }
</style>
```

### max-height 속성

- max-height 속성은 해당 HTML 요소가 가질 수 있는 최대 높이(height)를 설정합니다.
- 이 속성의 기본 설정값은 none이며, 해당 HTML 요소의 크기에 따라 높이가 자동으로 설정됩니다.
- max-height 속성으로 최대 높이를 설정하면, 해당 HTML 요소의 높이를 설정된 높이 이하로 제한합니다.
- 만약 해당 요소의 높이가 설정된 최대 높이보다 클 경우에는 수직 스크롤 바를 생성하게 됩니다.

  ```html
  <style>
    p {
      max-height: 50px;
      overflow: auto;
    }
  </style>
  ```

### min-height 속성

- min-height 속성은 지정된 HTML 요소가 가질 수 있는 최소 높이(height)를 설정합니다.
  이 속성의 기본 설정값은 0이며, 해당 HTML 요소의 높이에 제한을 두지 않겠다는 의미입니다.
- min-height 속성을 설정하면 해당 HTML 요소의 높이를 설정된 높이 이하로 제한합니다.
  즉 height 속성값이 min-height 속성값 이하로 낮아지지 않도록 합니다.
  이러한 min-height 속성값은 max-height 속성값과 height 속성값보다 먼저 적용됩니다.

```html
<style>
  p {
    min-height: 100px;
  }
</style>
```

---

### CSS 크기(dimension) 속성

| 속성       | 설명                                                      |
| ---------- | --------------------------------------------------------- |
| height     | 해당 HTML 요소의 높이를 설정함.                           |
| width      | 해당 HTML 요소의 너비를 설정함.                           |
| max-width  | 해당 HTML 요소가 가질 수 있는 최대 너비(width)를 설정함.  |
| min-width  | 해당 HTML 요소가 가질 수 있는 최소 너비(width)를 설정함.  |
| max-height | 해당 HTML 요소가 가질 수 있는 최대 높이(height)를 설정함. |
| min-height | 해당 HTML 요소가 가질 수 있는 최소 높이(height)를 설정함. |

---

## 박스 모델

- 모든 HTML 요소는 박스(box) 모양으로 구성되며, 이것을 박스 모델(box model)이라고 부릅니다.
- 박스 모델은 HTML 요소를 패딩(padding), 테두리(border), 마진(margin), 그리고 내용(content)으로 구분합니다.
  ![img_css_boxmodel imff.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/07be1d94-1c44-4208-8a55-2d03f32c61cb/978780c4-fdb3-49fa-b0e5-03e457a21dce/img_css_boxmodel_imff.png)

1. 내용(content) : 텍스트나 이미지가 들어있는 박스의 실질적인 내용 부분입니다.
2. 패딩(padding) : 내용과 테두리 사이의 간격입니다. 패딩은 눈에 보이지 않습니다.
3. 테두리(border) : 내용와 패딩 주변을 감싸는 테두리입니다.
4. 마진(margin) : 테두리와 이웃하는 요소 사이의 간격입니다. 마진은 눈에 보이지 않습니다.

   ```html
   <style>
     div {
       background-color: red;

       padding: 50px;

       border: 20px solid maroon;

       margin: 50px;
     }
   </style>
   ```

### height와 width 속성의 이해

- 모든 웹 브라우저에서 정확하게 HTML 요소들을 표현하려면 이러한 박스 모델이 어떻게 동작하는지 정확히 알아야만 합니다.
- CSS에서 height와 width 속성을 설정할 때 그 크기가 가르키는 부분은 내용(content) 부분만을 대상으로 합니다.
- HTML 요소의 height와 width 속성으로 설정된 높이와 너비에 패딩(padding), 테두리(border), 마진(margin)의 크기는 포함되지 않습니다.

  ```html
  <style>
    div {
      width: 320px;

      padding: 10px;

      border: 5px solid maroon;

      margin: 0;
    }
  </style>
  ```

### **HTML 요소의 높이와 너비 구하기**

![img_css_boxsize12.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/07be1d94-1c44-4208-8a55-2d03f32c61cb/a212c0ed-297e-4e53-b42c-3a93a33a6b28/img_css_boxsize12.png)

- 위의 그림에서 전체 너비(width)를 계산해 보면,

  width(70px) + left margin(10px) + left padding(5px) + right padding(5px) + right margin(10px) = 100px 이 됩니다.

- 즉, HTML 요소의 전체 너비(width)를 계산하는 공식은

  width + left padding + right padding + left border + right border + left margin + right margin 입니다.

- 또한, HTML 요소의 전체 높이(height)를 계산하는 공식은

  height + top padding + bottom padding + top border + bottom border + top margin + bottom margin 입니다.

- 이때 마진(margin) 영역의 크기는 눈으로 바로 확인할 수는 없을 것입니다.
  왜냐하면 마진이란 테두리(border)와 이웃하는 요소 사이의 간격이면서, 배경색의 영향을 받지 않기 때문입니다.
  하지만 HTML 요소가 차지하는 크기에는 포함됩니다.

> 💡 익스플로러 8과 그 이전 버전에서는 width나 height 속성으로 설정한 너비나 높이에 패딩과 테두리의 크기까지 포함됩니다.
> 이러한 차이점을 없애기 위해서는 반드시 HTML 문서에 <!DOCTYPE html>태그를 삽입해야만 합니다.
