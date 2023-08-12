<template>
  <h1 class="pb-10">Simple Form</h1>

  <h3>Form Input Display</h3>

  <br />

  <ul>
    <li v-for="item in error" v-bind:key="item">{{ item }} is not valid</li>
  </ul>

  <form class="pt-5" action="">
    <label class="pr-4" for="Email"> Email: </label>
    <input
      v-model="form.email"
      type="email"
      name="email"
      id="email"
      placeholder="Enter your email.."
      class="border-2 border-cyan-500"
    />

    <br />

    <br />

    <label class="pr-4" for="Password"> Password: </label>
    <input
      v-model="form.password"
      type="password"
      name="password"
      id="pasword"
      placeholder="Password"
      class="border-2 border-cyan-500"
    />
  </form>

  <br />

  <label class="pr-4" for="country">Country:</label>
  <select name="" id="" class="border border-cyan-700" v-model="form.country">
    <option value="Nigeria">Nigeria</option>
    <option value="USA">USA</option>
    <option value="Canada">Canada</option>
  </select>

  <br />
  <br />

  <h3>Gender</h3>
  <label for="Male">Male:</label>
  <input
    type="radio"
    value="male"
    name="gender"
    id="male"
    v-model="form.gender"
  />
  <br />

  <label for="Male">Female:</label>
  <input
    type="radio"
    value="female"
    name="gender"
    id="female"
    v-model="form.gender"
  />

  <br />
  <br />

  <h3>Technology</h3>
  <label class="pr-4" for="Java">Java:</label>
  <input
    type="checkbox"
    value="Java"
    name="gender"
    id="male"
    v-model="form.technology"
  />
  <br />

  <label class="pr-4" for="Node.JS">Node.JS:</label>
  <input
    type="checkbox"
    value="Node.JS"
    name="gender"
    id="female"
    v-model="form.technology"
  />

  <br />
  <br />

  <button
    v-on:click="login"
    type="button"
    class="border-2 rounded-lg p-1 border-cyan-700"
  >
    Login
  </button>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      form: {
        email: "",
        password: "",
        country: "",
        gender: "",
        technology: [],
      },
      error: [],
    };
  },

  methods: {
    login() {
      this.error = [];
      for (const item in this.form) {
        if (this.form[item] === "" || this.form[item].length == 0) {
          this.error.push(item);
        }
      }
      if (this.error.length === 0) {
        alert("Data has been submitted!");
      }
      console.warn(this.error);
    },
  },
};
</script>

<style scoped></style>
