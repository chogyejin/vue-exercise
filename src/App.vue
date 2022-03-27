<script>
export default {
  data() {
    return {
      text: '수정해보세요',
      checked: false,
      checkedNames: [],
      picked: '기호 1번',
      selected: 'A',
    }
  }
}
</script>

<template>
  <h1>글씨를 쳐보세요</h1>
  <input v-model="text"> <div>{{ text }}</div>

  <h2>체크박스</h2>
  <input type="checkbox" id="checkbox" v-model="checked" />
  <label for="checkbox">체크 여부: {{ checked }}</label>
  
  <h2>다중 체크박스</h2>
  <input type="checkbox" id="cheolsoo" value="김철수" v-model="checkedNames" />
  <label for="cheolsoo">김철수</label>
  <input type="checkbox" id="jihoon" value="박지훈" v-model="checkedNames" />
  <label for="jihoon">박지훈</label>
  <input type="checkbox" id="chadol" value="이차돌" v-model="checkedNames" />
  <label for="chadol">이차돌</label>
  <p>Checked names: <pre>{{ checkedNames }}</pre></p>

  <h2>input 라디오 타입</h2>
  <input type="radio" id="one" value="기호 1번" v-model="picked" />
  <label for="one">1번 김나나</label>
  <br>
  <input type="radio" id="two" value="기호 2번" v-model="picked" />
  <label for="two">2번 박기수</label>
  <br>
  <span>Picked: {{ picked }}</span>

  <h2>Select</h2>
  <select v-model="selected">
    <option disabled value="">하나 고르세요</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <div>{{ selected }} 선택</div>
</template>