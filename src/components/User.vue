<template>
  <h1>Child component</h1>

  <button
    v-on:click="getUser(userName)"
    class="border-2 rounded-full p-2 border-cyan-700"
  >
    Send username to Parent component
  </button>
</template>
<script>
export default {
  name: "User",
  data() {
    return {
      userName: "Peter",
    };
  },
  props: {
    getUser: Function,
  },
};
</script>
