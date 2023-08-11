<template>
  <h1 class="underline text-[30px] pb-10">CSS/Class binding</h1>

  <h3 :class="adjustStyle" class="pb-10">Hello world</h3>
  <button class="bg-blue-500 rounded-lg p-2" v-on:click="textBg = !textBg">
    Apply color
  </button>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      textBg: false,
    };
  },
  computed: {
    adjustStyle() {
      return { green: this.textBg, textColor: true, other: true };
    },
  },
};
</script>

<style scoped>
.green {
  background-color: green;
  width: 200px;
}
.textColor {
  color: red;
}
.other {
  height: 60px;
}
</style>
