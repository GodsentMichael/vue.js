<template></template>
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
