# **HTML 입력 양식**

## **Form 요소**

- 웹 페이지에서는 form 요소를 사용하여 사용자로부터 입력을 받을 수 있습니다.
  또한, 사용자가 입력한 데이터를 서버로 보낼 때에도 form 요소를 사용합니다.

- form 요소는 다음과 같은 문법으로 사용합니다.

  ```html
  <form action="처리할페이지주소" method="get|post"></form>
  ```

- action 속성은 입력받은 데이터를 처리할 서버 상의 스크립트 파일의 주소를 명시한다.
  이렇게 전달받은 데이터를 처리하는 스크립트 파일을 폼 핸들러(form-handler)라고 한다.
  method 속성은 입력받은 데이터를 서버에 전달할 방식을 명시한다.
- 따라서 사용자가 form 요소를 통해 입력한 데이터는 action 속성에 명시된 위치로 method 속성의 방식을 통해 전달된다

## **method 속성**

- method 속성을 통해 명시할 수 있는 form 요소의 전달 방식은 GET 방식과 POST 방식으로 나눠집니다.
- GET 방식은 주소에 데이터(data)를 추가하여 전달하는 방식입니다.
  데이터가 주소 입력창에 그대로 나타나며, 전송할 수 있는 데이터의 크기 또한 제한적입니다.
  따라서 검색 엔진의 쿼리(query)와 같이 크기가 작고 중요도가 낮은 정보를 보낼 때 주로 사 용합니다.
- POST 방식은 데이터(data)를 별도로 첨부하여 전달하는 방식입니다. 데이터가 외부에 드러나지 않으며, 전송할 수 있는 데이터의 크기 또한 제한이 없습니다.
  따라서 보안성 및 활용성이 GET 방식보다 좋습니다.

## **다양한 타입의 input 요소**

- HTML에서는 다양한 타입의 input 요소를 사용하여 사용자로부터 입력을 받을 수 있습니다.
  HTML에서 사용할 수 있는 대표적인 input 요소의 타입은 다음과 같습니다.
  1. 텍스트 입력(text)
  2. 비밀번호 입력(password)
  3. 라디오 버튼(radio)
  4. 체크박스(checkbox)
  5. 파일 선택(file)
  6. 선택 입력(select)
  7. 문장 입력(textarea)
  8. 버튼 입력(button)
  9. 전송 버튼(submit)
  10. 필드셋(fieldset)

## 텍스트 입력

- `<input>`태그의 type 속성값을 "text"로 설정하면, 사용자로부터 한 줄의 텍스트를 입력받을 수 있습니다.

```html
<form action="/examples/media/request.php">
  검색할 내용을 입력하세요 :
  <input type="text" name="search" />
</form>
```

## **비밀번호 입력**

- `<input>`태그의 type 속성값을 "password"로 설정하면, 사용자로부터 비밀번호를 입력받을 수 있습니다.
  비밀번호를 입력받기 때문에 화면에는 입력받은 문자나 숫자 대신 별표나 작은 원 모양이 표시됩니다.

  ```html
  <form>
    사용자 : <br /><input type="text" name="username" /><br />

    비밀번호 : <br /><input type="password" name="password" />
  </form>
  ```

## 라디오 버튼

- `<input>`태그의 type 속성값을 "radio"로 설정하면, 사용자로부터 여러 개의 옵션(option) 중에서 단 하나의 옵션만을 입력받을 수 있습니다.
  이때 서버로 정확한 입력을 전송하기 위해서는 반드시 모든 input 요소의 name 속성이 같아야 합니다.

  ```html
  <form>
    <input type="radio" name="lecture" value="html" checked /> HTML <br />

    <input type="radio" name="lecture" value="css" /> CSS <br />

    <input type="radio" name="lecture" value="java" /> JAVA <br />

    <input type="radio" name="lecture" value="cpp" /> C++
  </form>
  ```

- checked 속성을 이용하여 여러 개의 옵션 중에서 처음에 미리 선택되는 옵션을 지정할 수 있습니다.

> 💡 정확한 입력값 전송을 위해서 radio 타입의 모든 input 요소가 반드시 같은 name 속성을 가지고 있어야 합니다.

## 체크박스

- `<input>`태그의 type 속성값을 "checkbox"로 설정하면, 사용자로부터 여러 개의 옵션 중에서 다수의 옵션을 입력받을 수 있습니다.
- 체크박스는 라디오 버튼과는 달리 여러 개의 옵션을 한 번에 입력받을 수 있습니다.
- 이때 서버로 정확한 입력을 전송하기 위해서는 반드시 모든 input 요소의 name 속성이 같아야 합니다.

  ```html
  <form>
    <input type="checkbox" name="lecture" value="html" checked /> HTML <br />

    <input type="checkbox" name="lecture" value="css" /> CSS <br />

    <input type="checkbox" name="lecture" value="java" /> JAVA <br />

    <input type="checkbox" name="lecture" value="cpp" disabled /> C++
  </form>
  ```

- checked 속성을 이용하여 여러 개의 옵션 중에서 처음에 미리 선택되는 옵션을 지정할 수 있습니다.
  - 또한, disabled 속성을 이용하여 해당 옵션을 선택할 수 없게 설정할 수도 있습니다.

## 파일 선택

- `<input>`태그의 type 속성값을 "file"로 설정하면, 사용자로부터 파일을 전송받을 수 있습니다.

  ```html
  <form>
    <input type="file" name="upload_file" accept="image/*" />
  </form>
  ```

- accept 속성을 이용하여 입력받을 수 있는 파일의 확장자 및 종류를 명시할 수 있습니다.

## 선택 입력

- select 요소는 여러 개의 옵션이 드롭다운 리스트(drop-down list)로 되어 있으며, 그중에서 단 하나의 옵션만을 입력받을 수 있습니다.
- option 요소는 드롭다운 리스트에서 선택할 수 있는 각각의 옵션을 명시합니다.

  ```html
  <select name="fruit">
    <option value="apple">사과</option>

    <option value="orange" selected>귤</option>

    <option value="strawberry">딸기</option>

    <option value="peach">복숭아</option>
  </select>
  ```

- selected 속성을 이용하여 드롭다운 리스트 중에서 처음에 미리 선택되는 옵션을 지정할 수 있습니다.

## 문장 입력

- textarea 요소는 사용자로부터 여러 줄의 텍스트를 입력받을 수 있습니다.

  ```html
  <textarea name="message" rows="5" cols="30">
  
      여기에 적으세요.
  
  </textarea>
  ```

- rows 속성과 cols 속성을 이용하여 textarea 요소의 크기를 자유롭게 지정할 수 있습니다.

## 버튼

- button 요소는 사용자가 누를 수 있는 버튼을 나타냅니다.

  ```html
  <button type="button" onclick="alert('버튼을 클릭하셨군요!')">
    버튼을 눌러주세요.
  </button>
  ```

## 전송 버튼

- `<input>`태그의 type 속성값을 "submit"으로 설정하면, 사용자로부터 입력받은 데이터(data)를 서버의 폼 핸들러로 제출하는 버튼을 만들 수 있습니다.
- 폼 핸들러(form-handler)란 입력받은 데이터를 처리하기 위한 서버 측의 웹 페이지를 의미합니다.

  이러한 폼 핸들러의 주소는 form 요소의 action 속성을 이용하여 명시할 수 있습니다.

```html
<form action="/examples/media/request.php">
  어릴 때 자신의 별명을 적어주세요 : <br />

  <input type="text" name="nickname" value="별명" /><br /><br />

  <input type="submit" value="전송" />
</form>
```

## **필드셋(fieldset)**

- fieldset 요소는 form 요소와 관련된 데이터들을 하나로 묶어주는 역할을 합니다.
  legend 요소는 fieldset 요소 안에서만 사용할 수 있으며, fieldset 요소의 제목을 나타냅니다.

  ```html
  <form action="/examples/media/request.php">
    <fieldset>
      <legend>입력 양식</legend>

      이름 : <br />

      <input type="text" name="username" /><br />

      이메일 : <br />

      <input type="text" name="email" /><br /><br />

      <input type="submit" value="전송" />
    </fieldset>
  </form>
  ```

> 💡 **HTML5에서 추가된 다양한 타입의 input 요소**

1. datalist 요소
2. keygen 요소
3. output 요소

---

## **Input 요소의 속성**

## input 요소의 속성란?

- input 요소의 여러 속성을 사용하면 사용자가 입력하는 방식을 더욱 다양하게 제어할 수 있습니다.

## **value 속성**

- value 속성은 input 요소의 입력 필드(input field)에 나타나는 초깃값을 설정합니다.

  ```html
  <form>
    이름 : <br /><input type="text" name="student_name" /><br />

    학번 : <br /><input type="text" name="student_id" /><br />

    학과 : <br /><input
      type="text"
      name="department"
      value="컴퓨터공학과"
    /><br />
  </form>
  ```

## **readonly 속성**

- readonly 속성은 사용자가 입력 필드를 볼 수는 있으나, 수정할 수는 없도록 설정합니다.
- disabled 속성과 다른 점은 전송 버튼(submit)을 누르면 초깃값이 서버로 전송된다는 점입니다.

  ```html
  <form>
    이름 : <br /><input type="text" name="student_name" /><br />

    학번 : <br /><input type="text" name="student_id" /><br />

    학과 : <br /><input
      type="text"
      name="department"
      value="컴퓨터공학과"
      readonly
    /><br />
  </form>
  ```

## **disabled 속성**

- disabled 속성은 사용자가 입력 필드를 아예 사용할 수 없도록 설정합니다.
  disabled 속성이 설정된 입력 필드는 사용할 수도 없고, 클릭할 수도 없습니다.
  또한, readonly 속성과는 달리 전송 버튼(submit)을 눌러도 초깃값이 서버로 전송되지 않습니다.

```html
<form>
  이름 : <br /><input type="text" name="student_name" /><br />

  학번 : <br /><input type="text" name="student_id" /><br />

  학과 : <br /><input
    type="text"
    name="department"
    value="컴퓨터공학과"
    disabled
  /><br />
</form>
```

### size 속성

- size 속성은 입력 필드에 보여지는 input 요소의 크기(size)를 설정합니다.
- maxlength 속성과는 달리 입력 필드가 한 번에 보여줄 수 있는 문자의 최대 개수만을 의미합니다.
- 따라서 입력될 수 있는 문자의 최대 길이는 maxlength 속성값에 따라 달라지며, size 속성과는 전혀 무관합니다.

  ```html
  <form>
    이름 : <br /><input
      type="text"
      name="student_name"
      value="홍길동"
      size="30"
    /><br />

    학번 : <br /><input type="text" name="student_id" /><br />
  </form>
  ```

---
