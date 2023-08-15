<template>
<h2>The Count: {{ count }}</h2>

<button v-on:click="count=count+1">+</button>

<br>

<button v-on:click="count=count-1">-</button>
</template>

<script>
export default {
  name: "Home",

  data() {
    return {
      count: 0
    };
  },

watch:{
  count (val, prev) {
    if(val > 10 && val > prev){
      alert("Stop counting!!")
      this.count = 0
    }
  }
}

};
</script>

<style scoped></style>
