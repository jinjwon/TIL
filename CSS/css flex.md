# CSS Flex

- CSS Flexbox (Flexible Box Layout)는 웹 페이지의 레이아웃을 효율적으로 다루기 위한 CSS 레이아웃 모듈 중 하나입니다. Flexbox를 사용하면 요소 간의 공간 배분 및 정렬을 더 쉽게 제어할 수 있습니다. Flexbox는 주로 수평 중심으로 요소를 정렬하거나 요소 간 간격을 조정하는 데 사용됩니다.

> 이 기술을 현재 사용해도 좋을지는 아래 페이지를 참고하셔요.
>
> - http://caniuse.com/#search=flex
> - 강의 및 자료 포함 https://www.opentutorials.org/course/2418/13526

**Flexbox를 사용하는 기본 개념과 속성을 알려드리겠습니다:**

1. Flex Container (부모 요소):

   - Flexbox 레이아웃을 사용하려면 먼저 부모 요소에 **`display: flex`** 또는 **`display: inline-flex`** 속성을 설정해야 합니다. 이렇게 하면 해당 요소가 Flex Container가 됩니다

     ```css
     .container {
       display: flex;
     }
     ```

2. Flex Items (자식 요소):

   - Flex Container 안에 있는 모든 자식 요소는 Flex Items로 간주됩니다.
   - Flex Items는 Flex Container 내에서 자동으로 가로로 정렬됩니다.

   ```css
   .item {
     /* Flex Item 속성은 여기에 추가합니다. */
   }
   ```

3. 주요 Flex Container 속성:
   - **`flex-direction`**: Flex Container의 주축(main axis)을 설정합니다. 기본값은 **`row`**입니다.
   - **`justify-content`**: 주축을 따라 Flex Items를 정렬합니다.
   - **`align-items`**: 교차 축(cross axis)을 따라 Flex Items를 정렬합니다.
   - **`flex-wrap`**: Flex Items가 한 줄에 모두 맞지 않을 때 줄 바꿈 여부를 설정합니다.
4. 주요 Flex Item 속성:
   - **`flex`**: Flex Items의 크기 및 분배를 제어합니다.
   - **`order`**: Flex Items의 순서를 변경합니다.

**간단한 Flexbox 레이아웃의 예시:**

```css
.container {
  display: flex;
  flex-direction: row; /* 기본값 */
  justify-content: center; /* 주축을 중앙에 정렬 */
  align-items: center; /* 교차 축을 중앙에 정렬 */
}

.item {
  flex: 1; /* 모든 Flex Items를 동일한 크기로 설정 */
  order: 2; /* Flex Items의 순서를 변경 */
}
```

- Flexbox를 사용하면 복잡한 레이아웃도 더 쉽게 다룰 수 있으며, 반응형 웹 디자인을 구현하는 데 유용합니다. Flexbox의 속성과 기능을 이해하고 익히면 웹 페이지의 레이아웃을 더 효율적으로 관리할 수 있습니다.

https://www.notion.so/d113852c5a1e4c2aa78220a13255a568?pvs=4#1878b9101c4340eea69c3f465984648d

---
