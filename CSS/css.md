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

---

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
  ![img_css_boxmodel imff.png](https://www.tcpschool.com/lectures/img_css_boxmodel.png)

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

![img_css_boxsize](https://www.tcpschool.com/lectures/img_css_boxsize.png)

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
