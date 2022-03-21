<script>
export default {
  data() {
    return {
      show: true,
      list: [{ number: 1 }, { number: 2 }, { number: 3 }],
    };
  },
  methods: {
    stopPush() {
      console.log("12312");
    },
  },
};
</script>

<template>
  <button @click="show = !show">show 토글</button>
  <button @click="list.push({ number: list.length + 1 })">숫자 push</button>
  <button @click="list.pop()">숫자 pop</button>
  <button @click="list.reverse()">뒤집기</button>

  <ul v-if="show && list.length">
    <li v-for="(item, index) of list" v-bind:key="index">{{ item.number }}</li>
  </ul>
  <p v-else-if="list.length">숫자는 있으니까 show 토글 켜요</p>
  <p v-else>숫자 없음</p>
</template>
