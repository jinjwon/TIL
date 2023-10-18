# CSS 글꼴

- CSS에서 사용할 수 있는 font 속성은 다음과 같습니다.
  1. font-family
  2. font-style
  3. font-variant
  4. font-weight
  5. font-size

## CSS 글꼴 집합(font-family)

- CSS에는 두 가지의 글꼴 집합(font family)이 존재합니다.
  - font family : 특정 글꼴 집합 ("Times", "Courier" 등)
  - generic family : 비슷한 모양을 가지는 글꼴 집합 ("Serif", "Monospace" 등)

## font-family 속성

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

## font-style 속성

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

## font-variant 속성

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

## font-weight 속성

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

## font-size 속성

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

## font-size의 크기 단위

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

## **CSS font 속성**

| 속성         | 설명                                                                          |
| ------------ | ----------------------------------------------------------------------------- |
| font         | 모든 font 속성을 이용한 스타일을 한 줄에 설정할 수 있음.                      |
| font-family  | 텍스트의 글꼴 집합(font family)을 설정함.                                     |
| font-style   | 주로 이탤릭체를 사용하기 위해 사용함.                                         |
| font-variant | 텍스트에 포함된 영문자 중 소문자만을 작은 대문자(small-caps) 글꼴로 변경시킴. |
| font-weight  | 텍스트를 얼마나 두껍게 표현할지를 설정함.                                     |
| font-size    | 텍스트의 크기를 설정함.                                                       |

---
