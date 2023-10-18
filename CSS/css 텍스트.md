# CSS 텍스트

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

## color속성

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

## **direction 속성**

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

## **letter-spacing 속성**

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

## **word-spacing 속성**

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

## text-align 속성

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

## text-decoration 속성

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

## text-transform 속성

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

## line-height 속성

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

## text-shadow 속성

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
