# CSS 배경

- 웹 페이지뿐만 아니라 HTML 요소는 모두 각자의 배경을 가지고 있습니다.
  CSS의 background 속성은 이러한 각 요소의 배경에 다양한 효과를 줄 수 있게 해줍니다.

- CSS에서 사용할 수 있는 background 속성은 다음과 같습니다.

1. background-color
2. background-image
3. background-repeat
4. background-position
5. background-attachment

## **background-color 속성**

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

## **background-image 속성**

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

## **background-position 속성**

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

## background-attachment 속성

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

## background 속성 한 번에 적용하기

- 위에서 언급한 모든 background 속성을 이용한 스타일을 한 줄에 설정할 수 있습니다.

  ```css
  <style>

      body { background: #FFCCCC url("/examples/images/img_man.png") no-repeat left bottom fixed; }

  </style>
  ```

## **CSS background 속성**

| 속성                  | 설명                                                           |
| --------------------- | -------------------------------------------------------------- |
| background            | 모든 background 속성을 이용한 스타일을 한 줄에 설정할 수 있음. |
| background-color      | HTML 요소의 배경색을 설정함.                                   |
| background-image      | HTML 요소의 배경 이미지를 설정함.                              |
| background-repeat     | 설정된 배경 이미지의 반복 유무를 설정함.                       |
| background-position   | 반복되지 않는 배경 이미지의 상대 위치를 설정함.                |
| background-attachment | 배경 이미지를 스크롤과는 무관하게 해당 위치에 고정시킴.        |

---
