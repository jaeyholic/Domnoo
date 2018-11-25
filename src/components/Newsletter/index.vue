<template>
  <div class="container newsl_container">
    <h2>Join our newsletter</h2>
    <div class="form">
      <input type="text" v-model="email">
      <button @click="submitHandler">Subscribe</button>
    </div>
    <div class="error_label">
      {{ error }}
    </div>
    <div class="success_label">
      {{ success }}
    </div>
    <div class="small">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur culpa, impedit molestiae minus ad ducimus reiciendis assumenda necessitatibus fuga consequuntur ipsa vero asperiores distinctio error.</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      error: "",
      success: ""
    };
  },
  methods: {
    validate(email) {
      let valid = [true, ""];
      if (!/\S+@\S+\.\S+/.text(email)) {
        valid = [false, "Enter a valid email"];
      }
      if (email === "") {
        valid = [false, "its empty"];
      }
      return valid;
    },
    submitHandler() {
      let valid = this.validate(this.email);
      if (valid[0]) {
        this.error = "";
      } else {
        this.error = valid[1];
      }
    }
  }
};
</script>

<style scoped>
</style>