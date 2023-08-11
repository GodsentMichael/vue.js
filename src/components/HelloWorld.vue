<template>
  <h1 class="underline text-[30px] pb-10">Props in Vue</h1>

  <Student name="Godsent" />
  <Teacher :name="name" />
</template>

<script>
import Student from "./Student.vue";
import Teacher from "./Teacher.vue";
export default {
  name: "Home",
  data() {
    return {
      name: "Bruce",
    };
  },
  components: {
    Student,
    Teacher,
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
