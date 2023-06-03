<template>
  <main class="main_memo">
    <ol>
      <li v-for="(memo,i) in data" :key="i">{{ memo }}</li>
    </ol>
  </main>
</template>

<script>
export default {
  name: "MainVue",
  setup() {
    const data = [
      "메모내용1",
      "메모내용2",
      "메모내용3",
      "메모내용4",
      "메모내용5",
      "메모내용6",
    ];
    return {data}
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