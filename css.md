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

![style color 자료.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/830fd546-9d9a-4eea-a2d7-6b0500b23768/style_color_%EC%9E%90%EB%A3%8C.jpg)

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
