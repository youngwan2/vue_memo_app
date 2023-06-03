<template>
  <main class="main_memo">
    <input type="text" @input="valueAdd($event.target.value)" />
    <button @click="add(input)">추가</button>
    <ol>
      <li v-for="(memo, i) in data" :key="i">{{ memo }}</li>
    </ol>
  </main>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "MainVue",
  setup() {
    const data = reactive([
      "메모내용1",
      "메모내용2",
      "메모내용3",
      "메모내용4",
      "메모내용5",
    ]);

    const input = "";
    return { data, input };
  },

  methods: {
    // 사용자가 입력창에 텍스트를 입력하면 전달받은 값을 input에 저장함
    valueAdd(value) {
      this.input = value;
    },
    add(value) {
      console.log(value);
      this.data.push(value);
      console.log(this.data);
    },
  },
};
</script>

<style lang="scss" scoped>
.main_memo ol {
  width: 100%;

  li {
    width: 100%;
    padding: 15px;
    margin: 5px;
  }
}
</style>