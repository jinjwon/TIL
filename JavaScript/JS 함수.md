# JS 함수

- 함수는, 특정 코드를 하나의 명령으로 실행 할 수 있게 해주는 기능입니다.

- 예를 들어서, 우리가 특정 값들의 합을 구하고 싶을 때는 다음과 같이 코드를 작성합니다.

```jsx
const a = 1;
const b = 2;
const sum = a + b;
```

- 한번, 이 작업을 함수로 만들어보겠습니다.

```jsx
function add(a, b) {
  return a + b;
}

const sum = add(1, 2);
console.log(sum);
```

- 결과는 3이 됩니다.

- 함수를 만들 때는 `function` 키워드를 사용하며, 함수에서 어떤 값을 받아올지 정해주는데 이를 파라미터(매개변수)라고 부릅니다.
- 함수 내부에서 `return` 키워드를 사용하여 함수의 결과물을 지정 할 수 있습니다.  
   추가적으로, `return` 을 하게 되면 함수가 끝납니다. 만약 다음과 같이 코드가 작성된다면, return 아래의 코드는 호출이 안됩니다.

```jsx
function add(a, b) {
  return a + b;
  console.log("호출이 되지 않는 코드!");
}

const sum = add(1, 2);
console.log(sum);
```

---

## 화살표 함수

- 함수를 선언하는 방식 중 또 다른 방법은 화살표 함수 문법을 사용 하는 것 입니다.

```jsx
const add = (a, b) => {
  return a + b;
};

console.log(add(1, 2));
```

- `function` 키워드 대신에 `=>` 문자를 사용해서 함수를 구현했는데요, 화살표의 좌측에는 함수의 파라미터, 화살표의 우측에는 코드 블록이 들어옵니다.

- 그런데, 만약에 위와 같이 코드 블록 내부에서 바로 return 을 하는 경우는 다음과 같이 줄여서 쓸 수도 있습니다.

```jsx
const add = (a, b) => a + b;
console.log(add(1, 2));
```

- 아까 만들었던 getGrade 함수처럼 여러 줄로 구성되어있는 경우에는 코드 블록을 만들어야합니다.

```jsx
const getGrade = (score) => {
  if (score === 100) {
    return "A+";
  } else if (score >= 90) {
    return "A";
  } else if (score === 89) {
    return "B+";
  } else if (score >= 80) {
    return "B";
  } else if (score === 79) {
    return "C+";
  } else if (score >= 70) {
    return "C";
  } else if (score === 69) {
    return "D+";
  } else if (score >= 60) {
    return "D";
  } else {
    return "F";
  }
};
const grade = getGrade(90);
console.log(grade);
```

- 화살표 함수와 일반 function 으로 만든 함수와의 주요 차이점은 화살표 함수에서 가르키는 this 와 function 에서 가르키는 this 가 서로 다르다는 건데요, 이에 대한 자세한 내용은 나중에 알아보도록 하겠습니다.
