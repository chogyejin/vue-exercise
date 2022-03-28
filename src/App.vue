<!--
Here we show the simplest possible component which accepts a prop and renders it.
Learn more about components in the guide!
-->

<script>
import TodoItem from "./components/TodoItem.vue";

export default {
  components: {
    TodoItem,
  },
  data() {
    return {
      todoList: [
        { id: 0, text: "과제 1" },
        { id: 1, text: "영화 보기" },
        { id: 2, text: "산책하기" },
      ],
    };
  },
};
</script>

<template>
  <h2>할 일 목록</h2>
  <ol>
    <!-- v-bind 생략한 형태로 적음 -->
    <TodoItem v-for="item in todoList" :todo="item" :key="item.id"></TodoItem>
  </ol>
</template>
