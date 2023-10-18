# CSS 링크

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

## 링크(link)의 상태

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

## 링크를 활용한 버튼(Button)

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
