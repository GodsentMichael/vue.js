<template>
  <Child>
    <template v-slot:header>
      <!-- <h1 class="justify-center text-center items-center">Peter</h1> -->
    </template>

    <template v-slot:main>
      <h1 class="justify-center text-center items-center">Holla!</h1>
    </template>
    <template v-slot:footer>
      <button class="justify-center border p-1 rounded-lg border-red-600 text-center items-center">
        Buy Now
      </button>
    </template>
  </Child>
  <Child>
    <template v-slot:header>
      <h1 class="justify-center text-center items-center">Michael</h1>
    </template>

    <template v-slot:main>
      <h1 class="justify-center text-center items-center">Code Step By Step</h1>
    </template>
    <template v-slot:footer>
      <button class="justify-center border p-1 rounded-lg border-red-600 text-center items-center">
       Get It
      </button>
    </template>
  </Child>
  <Child >
    <template v-slot:header>
      <h1 class="justify-center text-center items-center">Lucas</h1>
    </template>

    <template v-slot:main>
      <h1 class="justify-center text-center items-center">Code Step By Step</h1>
    </template>
    <template v-slot:footer class="justify-center items-center">
      <button class="justify-center border p-1 rounded-lg border-red-600 text-center items-center">
        Pay now
      </button>
    </template>
  </Child>
</template>
<script>
import Child from "../components/Child.vue";
export default {
  name: "Home",
  components:{
    Child,
  } 
    
};
</script>

<style scoped></style>
