<template>
  <h1 class="underline text-[30px] pb-10">Username: {{ name }}</h1>

  <User :getUser="getUserName" />
</template>

<script>
import User from "./User.vue";
export default {
  name: "Home",
  data() {
    return {
      name: "",
    };
  },
  components: {
    User,
  },
  methods: {
    getUserName(name) {
      this.name = name;
    },
  },
};
</script>

<style scoped></style>
