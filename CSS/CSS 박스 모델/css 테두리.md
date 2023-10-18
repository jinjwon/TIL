# 테두리

## 테두리(border)이란?

- border 속성은 내용(content)과 패딩(padding) 영역을 둘러싸는 테두리의 스타일을 설정한다.
  ![img_css_boxmodel_border123.png](https://www.tcpschool.com/lectures/img_css_boxmodel_border.png)

## border-style 속성

- border-style 속성을 이용하면 테두리(border)를 다양한 모양으로 설정할 수 있습니다.

  1. dotted : 테두리를 점선으로 설정함.
  2. dashed : 테두리를 약간 긴 점선으로 설정함.
  3. solid : 테두리를 실선으로 설정함.
  4. double : 테두리를 이중 실선으로 설정함.
  5. groove : 테두리를 3차원인 입체적인 선으로 설정하며, border-color 속성값에 영향을 받음.
  6. ridge : 테두리를 3차원인 능선효과가 있는 선으로 설정하며, border-color 속성값에 영향을 받음.
  7. inset : 테두리를 3차원인 내지로 끼운 선으로 설정하며, border-color 속성값에 영향을 받음.
  8. outset : 테두리를 3차원인 외지로 끼운 선으로 설정하며, border-color 속성값에 영향을 받음.
  9. none : 테두리를 없앰.
  10. hidden : 테두리가 존재하기는 하지만 표현되지는 않음.

      ```html
      <style>
        .dotted {
          border-style: dotted;
        }

        .dashed {
          border-style: dashed;
        }

        .solid {
          border-style: solid;
        }

        .double {
          border-style: double;
        }

        .groove {
          border-style: groove;
        }

        .ridge {
          border-style: ridge;
        }

        .inset {
          border-style: inset;
        }

        .outset {
          border-style: outset;
        }

        .none {
          border-style: none;
        }

        .hidden {
          border-style: hidden;
        }

        .mix {
          border-style: solid dashed dotted double;
        }
      </style>
      ```

## border-width 속성

- border-width 속성은 테두리(border)의 두께를 설정합니다.
- px, em, cm 등과 같은 CSS 크기 단위를 이용하여 두께를 직접 설정할 수 있습니다.
- 또한, 미리 설정해 놓은 예약어인 thin, medium, thick을 사용하여 설정할 수도 있습니다.

  ```html
  <style>
    .dottedA {
      border-style: dotted;
      border-width: 2px;
    }

    .dottedB {
      border-style: dotted;
      border-width: 5px;
    }

    .dashedA {
      border-style: dashed;
      border-width: thin;
    }

    .dashedB {
      border-style: dashed;
      border-width: thick;
    }

    .doubleA {
      border-style: double;
      border-width: 5px;
    }

    .doubleB {
      border-style: double;
      border-width: thick;
    }

    .mix {
      border-style: solid;
      border-width: 1px 2px 10px thick;
    }
  </style>
  ```

### border-color 속성

- border-color 속성은 테두리(border)의 색상을 설정합니다.
- 기본적인 color 속성값들뿐만 아니라 투명한 선을 나타내는 transparent 속성값을 사용할 수도 있습니다.
- border-color 속성값이 설정되지 않으면 해당 요소의 color 속성값을 그대로 물려받습니다.

  ```html
  <style>
    .red {
      border-color: red;
    }

    .green {
      border-color: rgb(0, 255, 0);
    }

    .blue {
      border-color: #0000ff;
    }

    .mix {
      border-color: red green blue maroon;
    }

    .color {
      color: teal;
    }
  </style>
  ```

### 테두리(border)의 개별 설정

- CSS를 사용하면 테두리의 위쪽, 오른쪽, 아래쪽, 왼쪽 부분에 대하여 개별적으로 스타일을 적용할 수 있습니다.

  ```html
  <style>
    .mixA {
      border-top-style: dotted;

      border-right-style: double;

      border-bottom-style: dotted;

      border-left-style: double;
    }

    .mixB {
      border-style: dotted double;
    }
  </style>
  ```

- 4개의 border-style 속성값을 가질 때는 top, right, bottom, left 순으로 설정합니다.
  ex) border-style: dotted dashed solid double;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)
  border-style-top: dotted;
  border-style-right: dashed;
  border-style-bottom: solid;
  border-style-left: double;
- 3개의 border-style 속성값을 가질 때는 top, right와 left, bottom 순으로 설정합니다.
  ex) border-style: dotted dashed solid;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)
  border-style-top: dotted;
  border-style-right: dashed;
  border-style-bottom: solid;
  border-style-left: dashed;
- 2개의 border-style 속성값을 가질 때는 top과 bottom, right와 left 순으로 설정합니다.
  ex) border-style: dotted dashed;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)
  border-style-top: dotted;
  border-style-right: dashed;
  border-style-bottom: dotted;
  border-style-left: dashed;
- 1개의 border-style 속성값을 가질 때는 모든 테두리의 스타일을 같게 설정합니다.
  ex) border-style: dotted;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)
  border-style-top: dotted;
  border-style-right: dotted;
  border-style-bottom: dotted;
  border-style-left: dotted;

### 테두리 축약 표현(border shorthand)

- 모든 border 속성을 이용한 스타일을 한 줄에 설정할 수 있습니다.

  ```html
  <style>
    .good {
      border: 3px solid teal;
    }

    .wrong {
      border: 5px teal;
    }
  </style>
  ```

> 💡 border 속성을 설정하기 위해서는 반드시 border-style 속성이 먼저 설정되어 있어야 합니다.

## **CSS border 속성**

| 속성                | 설명                                                       |
| ------------------- | ---------------------------------------------------------- |
| border              | 모든 border 속성을 이용한 스타일을 한 줄에 설정할 수 있음. |
| border-style        | 테두리(border)를 다양한 모양으로 설정함.                   |
| border-width        | 테두리(border)의 너비를 설정함.                            |
| border-color        | 테두리(border)의 색상을 설정함.                            |
| border-top          | 테두리(border)의 top 부분 속성을 한 번에 설정함.           |
| border-top-style    | 테두리(border)의 top 부분의 스타일을 설정함.               |
| border-top-width    | 테두리(border)의 top 부분의 너비를 설정함.                 |
| border-top-color    | 테두리(border)의 top 부분의 색상을 설정함.                 |
| border-right        | 테두리(border)의 right 부분 속성을 한 번에 설정함.         |
| border-right-style  | 테두리(border)의 right 부분의 스타일을 설정함.             |
| border-right-width  | 테두리(border)의 right 부분의 너비를 설정함.               |
| border-right-color  | 테두리(border)의 right 부분의 색상을 설정함.               |
| border-bottom       | 테두리(border)의 bottom 부분 속성을 한 번에 설정함.        |
| border-bottom-style | 테두리(border)의 bottom 부분의 스타일을 설정함.            |
| border-bottom-width | 테두리(border)의 bottom 부분의 너비를 설정함.              |
| border-bottom-color | 테두리(border)의 bottom 부분의 색상을 설정함.              |
| border-left         | 테두리(border)의 left 부분 속성을 한 번에 설정함.          |
| border-left-style   | 테두리(border)의 left 부분의 스타일을 설정함.              |
| border-left-width   | 테두리(border)의 left 부분의 너비를 설정함.                |
| border-left-color   | 테두리(border)의 left 부분의 색상을 설정함.                |

---
