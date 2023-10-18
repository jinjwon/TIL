# CSS 크기

## 크기(Dimension)란?

- CSS를 이용하면 HTML 요소의 크기를 마음대로 설정할 수 있습니다.
- CSS에서 크기 조절을 위해 사용할 수 있는 속성은 다음과 같습니다.
  1. height
  2. width
  3. max-width
  4. min-width
  5. max-height
  6. min-height

---

## height와 width 속성

- height와 width 속성은 HTML 요소의 높이와 너비를 각각 설정합니다.
- 이 속성의 기본 설정값은 auto이며, 웹 브라우저가 각 HTML 요소에 맞게 자동으로 높이와 너비를 설정해 줍니다.

  ```css
  <style>

      div { height: 200px; width: 500px; }

  </style>
  ```

## max-width 속성

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

## max-height 속성

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

## min-height 속성

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

## CSS 크기(dimension) 속성

| 속성       | 설명                                                      |
| ---------- | --------------------------------------------------------- |
| height     | 해당 HTML 요소의 높이를 설정함.                           |
| width      | 해당 HTML 요소의 너비를 설정함.                           |
| max-width  | 해당 HTML 요소가 가질 수 있는 최대 너비(width)를 설정함.  |
| min-width  | 해당 HTML 요소가 가질 수 있는 최소 너비(width)를 설정함.  |
| max-height | 해당 HTML 요소가 가질 수 있는 최대 높이(height)를 설정함. |
| min-height | 해당 HTML 요소가 가질 수 있는 최소 높이(height)를 설정함. |
