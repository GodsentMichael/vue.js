<template>
  <h1 class="underline text-[30px] pb-10">Username: {{ name }}</h1>

  <input type="text" name="" id="" ref="input" />
  <button v-on:click="getData">Click me</button>
</template>

<script>
import User from "./User.vue";
export default {
  name: "Home",
  // data() {
  //   return {
  //     name: "",
  //   };
  // },

  methods: {
    getData() {
      this.$refs.input.focus();
      this.$refs.input.value = "this is a test";
      this.$refs.input.style.color = "red";
      console.warn(this.$refs.input.value);
    },
  },
};
</script>

<style scoped></style>
