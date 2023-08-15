<template>
  <h1 class="flex Justify-center text-3xl items-center text-blue-400 pb-4">
    Teleport components
  </h1>

  <h3>Yeah!</h3>

  <teleport to="#footer">
    <Footer/>
  </teleport>

</template>
<script>
import Footer from "../components/Footer.vue";


export default {
  name: "Home",
  components: {
    Footer,
    
  },

  data() {
    return {
      tab: "Java",
    };
  },
};
</script>

<style scoped></style>
