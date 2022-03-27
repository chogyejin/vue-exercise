# vue-exercise

Refer to

- [Vue.js DOCS ](https://vuejs.org/guide/introduction.html)
- [Vue.js DOCS KOR](https://v3.ko.vuejs.org/guide/introduction.html)

## Setup

1. Install Vue.js : `npm init vue@latest`, set project config
2. Execute on VSCode : `cd <project-nane>`, `code .`
3. Run the project : `npm run dev`

- Vetur extension 설치

## Handling User Input

### Declarative Rendering(선언적 렌더링)

- templete 구문을 사용하여 DOM에서 데이터를 선언적으로 렌더링, 데이터가 반응형(reactive)이 됨

### Directive

- Vue의 특수 attribute, v- 접두어가 붙음
  - `v-bind:title`은 `:title`로 축약 가능
  - `v-on` directive로 Vue 인스턴스에서 이벤트 리스너를 추가할 수 있음
  - `@click` 문법은 `v-on:click`의 축약 가능
  - `@click.prevent`와 같이 common tasks를 수정하기도 한다.
- Two way Binding
  - `v-model` directive로 input 태그 입력과 앱 상태를 양방향 바인딩 가능
    - Form 요소(input-label, select)와 데이터 바인딩
    - label 태그의 for 속성은 input의 id 속성과 연결된다.
    - 다중 체크박스의 v-model directive는 같은 값으로 관리, value는 Checked names 배열에 들어갈 값

## Conditionals and Loops

- number property를 가지고 있는 object list를 이용하여 toggle, push, pop, reverse
- 조건문
  - `v-if`, `v-else-if`, `v-else`
- 반복문
  - `v-for`, `v-bind:key`
- Vue 엘리먼트가 Vue에 삽입/업데이트/제거될 때 자동으로 전환 효과(transition effects)가 적용된다.
