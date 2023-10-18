# CSS 선택자

- HTML 요소 선택자
- 아이디(id) 선택자
- 클래스(class) 선택자
- 그룹(group) 선택자

## HTML 요소 선택자

```<style>

        h2 { color: teal; text-decoration: underline; }

    </style>

    ...

    <h2>이 부분에 스타일을 적용합니다.</h2>
```

## 아이디(id) 선택자

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

## 클래스(class) 선택자

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

## 그룹(group) 선택자

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

---
