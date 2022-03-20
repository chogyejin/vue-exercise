<script>
export default {
  data() {
    return {
      message: "Hello World!",
      time: new Date().toLocaleString(),
    };
  },
  methods: {
    splitString() {
      if (typeof this.message !== "string") return;
      this.message = this.message.split(""); // string to array
    },
    reverseArray() {
      if (!Array.isArray(this.message)) return;
      this.message = this.message.reverse(); // reverse array
    },
    joinArray() {
      if (!Array.isArray(this.message)) return;
      this.message = this.message.join(""); // array to string
    },
    alertMessage() {
      alert("안녕");
    },
    appendBang() {
      if (Array.isArray(this.message)) return;
      this.message += "!";
    },
    notify() {
      alert("navigation was prevented.");
    },
  },
};
</script>

<template>
  <div>
    <span v-bind:title="time">
      여기에 마우스를 올려두고 잠시 기다리면 제목이 동적으로 바뀝니다!
    </span>
  </div>
  <div>
    <h1>{{ message }}</h1>
    <input v-model="message" />
  </div>
  <div><button @click="splitString">문자열을 배열로</button></div>
  <div><button @click="reverseArray">배열 뒤집기</button></div>
  <div><button @click="joinArray">배열을 문자열로</button></div>
  <div><button @click="alertMessage">안녕</button></div>
  <div><button @click="appendBang">Append "!"</button></div>
  <div>
    <a href="https://vuejs.org" @click.prevent="notify">
      A link with e.preventDefault()
    </a>
  </div>
</template>
