# 패딩

## 패딩(padding)이란?

- padding 속성은 내용(content)과 테두리(border) 사이의 간격인 패딩 영역의 크기를 설정합니다.
  이러한 패딩 영역은 background-color 속성으로 설정하는 배경색의 영향을 함께 받습니다.
- CSS를 사용하면 패딩 영역의 크기를 방향별로 따로 설정할 수 있습니다.

![img_css_boxmodel_padding22.png](https://www.tcpschool.com/lectures/img_css_boxmodel_padding.png)

## 패딩(padding) 속성

- CSS에서는 HTML 요소의 패딩 영역을 설정하기 위해 다음과 같은 속성을 제공합니다.

  1. padding-top
  2. padding-right
  3. padding-bottom
  4. padding-left

  ```html
  <style>
    div.pad {
      padding-top: 50px;

      padding-right: 10px;

      padding-bottom: 30px;

      padding-left: 100px;
    }
  </style>
  ```

## 패딩 축약 표현(padding shorthand)

- 모든 padding 속성을 이용한 스타일을 한 줄에 설정할 수 있습니다.

```html
<style>
  div.four {
    padding: 20px 50px 30px 50px;
  }

  div.three {
    padding: 20px 50px 30px;
  }
</style>
```

- 4개의 padding 속성값을 가질 때는 top, right, bottom, left 순으로 설정합니다.
  ex) padding: 10px 20px 30px 40px;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)

  padding-top: 10px;

  padding-right: 20px;

  padding-bottom: 30px;

  padding-left: 40px;

- 3개의 padding 속성값을 가질 때는 top, right와 left, bottom 순으로 설정합니다.
  ex) padding: 10px 20px 30px;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)

  padding-top: 10px;

  padding-right: 20px;

  padding-bottom: 30px;

  padding-left: 20px;

- 2개의 padding 속성값을 가질 때는 top과 bottom, right와 left 순으로 설정합니다.
  ex) padding: 10px 20px;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)

  padding-top: 10px;

  padding-right: 20px;

  padding-bottom: 10px;

  padding-left: 20px;

- 1개의 padding 속성값을 가질 때는 모든 패딩값을 같게 설정합니다.
  ex) padding: 10px;
- (위의 예제는 아래 4줄의 코드와 같은 의미를 가지고 있습니다.)
  padding-top: 10px;
  padding-right: 10px;
  padding-bottom: 10px;
  padding-left: 10px;

## **CSS padding 속성**

| 속성           | 설명                                                        |
| -------------- | ----------------------------------------------------------- |
| padding        | 모든 padding 속성을 이용한 스타일을 한 줄에 설정할 수 있음. |
| padding-top    | 윗쪽의 패딩(padding) 값을 설정함.                           |
| padding-right  | 오른쪽의 패딩(padding) 값을 설정함.                         |
| padding-bottom | 아래쪽의 패딩(padding) 값을 설정함.                         |
| padding-left   | 왼쪽의 패딩(padding) 값을 설정함.                           |

---
