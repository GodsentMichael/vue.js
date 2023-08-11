<template>
  <h1>Student name is :{{ name }}</h1>
</template>

<script>
export default {
  name: "Student",
  props: {
    name: String,
  },
};
</script>
