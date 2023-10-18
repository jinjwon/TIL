# CSS 테이블

- 테이블에 다음 속성을 사용하여 CSS 스타일을 적용할 수 있습니다.
  1. border
  2. border-collapse
  3. border-spacing
  4. caption-side
  5. empty-cells
  6. table-layout

## border 속성

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

## border-collapse 속성

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

## border-spacing 속성

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

## text-align 속성

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

## vertical-align 속성

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

## 다양한 형태의 테이블 예제

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

## **CSS table 속성**

| 속성            | 설명                                                                      |
| --------------- | ------------------------------------------------------------------------- |
| border          | 모든 border 속성을 이용한 스타일을 한 줄에 설정할 수 있음.                |
| border-collapse | 테이블의 테두리를 한 줄로 나타낼지를 설정함.                              |
| border-spacing  | 테이블 요소(th, td)간의 여백을 설정함.                                    |
| caption-side    | 테이블의 캡션(caption)을 설정함.                                          |
| empty-cells     | 테이블 내의 빈 셀(cell)들의 테두리 및 배경색을 표현할지 안 할지를 설정함. |
| table-layout    | 테이블에 사용되는 레이아웃 알고리즘을 설정함.                             |

---
