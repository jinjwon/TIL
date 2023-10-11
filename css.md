# **CSS이란?**

> CSS는 Cascading Style Sheets의 약자입니다.
>
> CSS는 HTML 요소들이 각종 미디어에서 어떻게 보이는가를 정의하는 데 사용되는 스타일 시트 언어입니다.
>
> HTML4 부터는 이러한 모든 서식 설정을 HTML 문서로부터 따로 분리하는 것이 가능해졌습니다.
>
> 오늘날 대부분의 웹 브라우저들은 모두 CSS를 지원하고 있습니다

## CSS 문법

![css 문법](https://www.tcpschool.com/lectures/img_css_syntax.png)

### CSS 선택자

- HTML 요소 선택자
- 아이디(id) 선택자
- 클래스(class) 선택자
- 그룹(group) 선택자

#### HTML 요소 선택자

```
<style>

        h2 { color: teal; text-decoration: underline; }

    </style>

    ...

    <h2>이 부분에 스타일을 적용합니다.</h2>

```

### 아이디(id) 선택자

- 아이디 선택자는 CSS를 적용할 대상으로 특정 요소를 선택할 때 사용합니다.
- 이 선택자는 웹 페이지에 포함된 여러 요소 중에서 특정 아이디 이름을 가지는 요소만을 선택해 줍니다.

```
<style>

    #heading { color: teal; text-decoration: line-through; }

</style>

...

<h2 id="heading">이 부분에 스타일을 적용합니다.</h2>
```

**💡 이렇게 중복된 아이디를 가지고 자바스크립트 작업을 하게 되면 오류가 발생합니다.**
**따라서 되도록이면 하나의 웹 페이지에 속하는 요소에는 다른 아이디 이름을 사용하거나클래스를 사용하는 것이 좋습니다.**
