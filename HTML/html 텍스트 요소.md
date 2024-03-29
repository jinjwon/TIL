# HTML 텍스트 요소

1. <태그이름> **- 시작 태그 -**
2. </태그이름> **- 종료 태그 -**

> `<img>` `<br>` `<hr>` 등과 같이 종료 태그 없이 시작 태그만을 가지는 태그를 빈 태그(empty tag)라고 합니다

## 제목

- HTML은 제목을 표현할 수 있는 다양한 크기의 `<h>`태그를 제공합니다.
  가장 큰 `<h1>`태그부터 가장 작은 `<h6>`태그까지 다양한 크기로 제목을 표현할 수 있습니다.
- `<h1>, <h2>, <h3>` 태그 제목을 표시한다

```html
<h1>제목 1크기</h1>
<h2>제목 2크기</h2>
<h3>제목 3크기</h3>
<h4>제목 4크기</h4>
```

> 💡 HTML 문서의 제목에 해당하는 부분을 `<big>`태그나 `<bold>`태그를 사용하여 표현하지 않도록 합니다.
> `<h>`태그의 위아래로는 약간의 여백이 자동으로 삽입됩니다.

---

## 단락

- 단락이란 내용상 끊어서 구분할 수 있는 하나하나의 부분을 의미하며, 문단이라고도 부릅니다.
  HTML에서는 `<p>`태그를 이용하여 이러한 단락을 표현합니다.

- `<p>`태그에 단락 넣어준다

  ```html
  <h1>제목1의 크기입니다!</h1>
  <p>단락 1</p>
  <p>단락 2</p>
  ```

- **텍스트(text) 서식 미리 정의하기**

  ```html
  <pre>
  
  줄을 나누고 싶어서
  
  이렇게 줄을 나누었다.
  
   
  
  과연     그대로     출력이     될까?
  
  </pre>
  ```

- **띄어쓰기, 수평 가로 구분선**
- 띄어쓰기

  ```html
  <br />태그(break line)를 사용하면 새로운 단락을 만들지 않고도 줄을 나눌 수
  있습니다. 이러한 <br />태그는 종료 태그가 없는 빈 태그(empty tag)입니다.
  ```

- 수평 가로 구분선

  ```html
  <p>저는 하나의 단락입니다.</p>

  <hr />

  <p>저는 하나의 단락입니다.</p>

  <hr />

  <p>저는 하나의 단락입니다.</p>
  ```

---

## 서식

- HTML은 텍스트(text)에 다양한 효과를 주는 여러 태그(tag)를 제공합니다.

- **강조 효과**
- HTML 문서에서 텍스트를 굵게 표현하고 싶을 때에는 `<b>`태그(bold text)나 `<strong>`태그를 사용하면 됩니다.

  ```html
  <p><b>"이 부분"</b>은 단순히 글씨가 굵은 부분이에요!</p>

  <p><strong>"이 부분"</strong>은 중요한 부분이라서 굵게 표현됐어요!</p>
  ```

- HTML 문서에서 이탤릭체를 표현하고 싶을 때에는 `<i>`태그(italic text)나 `<em>`태그(emphasized text)를 사용합니다.

---

- **하이라이팅 효과**
- `<mark>`태그는 텍스트에 하이라이팅(highlighting) 효과를 적용시켜 줍니다.

  ```html
  <p><mark>"이 부분"</mark>만 하이라이팅하고 싶어요.</p>
  ```

- **사입 효과**
- `<ins>`태그(insert)는 텍스트 밑에 가로줄을 만들어 마치 빈칸에 텍스트를 삽입한 것과 같은 효과를 내줍니다.

  ```html
  <p><ins>"밑줄 친 부분"</ins>에 들어갈 알맞은 말을 고르세요.</p>
  ```

---

## 인용구

- **짧은 인용구**
- 짧은 인용구는 `<q>` 태그(quotation)를 사용하여 표현할 수 있으며, 자동으로 앞뒤에 큰따옴표가 붙습니다.

  ```html
  <p><b>"이 부분"</b>은 단순히 글씨가 굵은 부분이에요!</p>

  <p><strong>"이 부분"</strong>은 중요한 부분이라서 굵게 표현됐어요!</p>
  ```

- **블록 인용구**

- 길이가 긴 인용문은 `<blockquote>`태그(block quatation)를 사용하여 표현할 수 있습니다.
- `<blockquote>`태그는 이러한 인용 부분을 별도의 단락으로 구분하여 나타냅니다.

  ```html
  <p>HTML의 정의</p>

  <blockquote>
    인터넷 서비스의 하나인 월드 와이드 웹을 통해 볼 수 있는 문서를 만들 때
    사용하는 프로그래밍 언어의 한 종류이다.
  </blockquote>
  ```

---

## 엔티티**(Entity)**

- HTML에는 미리 예약된 몇몇 문자가 있으며, 이러한 문자를 HTML 예약어(reserved characters)라고 부른다.

```html
&엔티티이름;
또는
&#엔티티숫자;
```

```html
<p></p>
<p>태그는 두 번째로 큰 제목을 나타내는 태그입니다.</p>

<p>&lt;p&gt;태그는 단락을 나타내는 태그입니다.</p>
```

위의 예시처럼 HTML 코드에서 사용된 꺾쇠괄호(<>)는 HTML 태그의 시작과 끝의 의미로 해석됩니다.

> 💡 엔티티(entity)의 이름은 대소문자를 구분합니다.

HTML에서 제공하는 대표적인 엔티티(entity)는 다음과 같습니다.

| 엔티티 문자 | 엔티티 이름 | 16진수 엔티티 숫자 | 설명              |
| ----------- | ----------- | ------------------ | ----------------- |
|             | &nbsp;      | &#160;             | 줄 바꿈 없는 공백 |
| <           | &lt;        | &#60;              | 보다 작은         |
| >           | &gt;        | &#62;              | 보다 큰           |
| &           | &amp;       | &#38;              | AND 기호          |
| "           | &quot;      | &#34;              | 큰따옴표          |
| '           | &apos;      | &#39;              | 작은따옴표        |

- 출처 : [출처](http://www.tcpschool.com/html/html_text_entities)

> 💡 HTML에서 사용할 수 있는 모든 엔티티에 대한 더 자세한 정보에는 W3C 공식 사이트를 방문하여 확인할 수 있다. ( [Character entity references in HTML =>](https://www.w3.org/TR/html4/sgml/entities.html) )

### 문자셋**(Character set)**

- 웹 브라우저가 HTML 문서를 정확하게 나타내기 위해서는 해당 문서가 어떠한 문자셋으로 저장되었는지를 알아야 합니다.
  따라서 HTML 문서가 저장될 때 사용된 문자셋에 대한 정보를 `<head>`태그 내의 `<meta>`태그에 명시합니다.

> 💡 HTML5에서 UTF-8의 경우 : `<meta charset="UTF-8">`

- 위의 두 예시는 해당 HTML 문서가 UTF-8 문자셋을 사용하여 저장되었음을 웹 브라우저에 알려준다.

### 문자셋의 종류

- 현재 사용되는 대표적인 문자셋(character set)은 다음과 같습니다.

1. ASCII : 가장 처음 만들어진 문자셋으로, 인터넷에서 사용할 수 있는 127개의 영문자와 숫자로 이루어져 있습니다.
2. ANSI : 윈도우즈에서 만든 문자셋으로, 총 256개의 문자 코드를 지원합니다.
3. ISO-8859-1 : 256개의 문자 코드를 지원하는 HTML4의 기본 문자셋입니다.
4. UTF-8 : 세상에 있는 거의 모든 문자를 표현할 수 있는 유니코드 문자를 지원하는 HTML5의 기본 문자셋입니다.

---
