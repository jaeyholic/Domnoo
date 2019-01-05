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
        this.addEmail(this.email)
      } else {
        this.error = valid[1];
      }
    },
    addEmail(email) {
      this.$http.get(`users.json?orderBy=\"email\"&&equalTo=\"${email}\"`)
      .then(response => {
        if(Object.getOwnPropertyNames(response.data).length === 0) {
          this.$http.post(`users.json`, {email: this.email})
          .then(response => {
            this.success = 'Thank you'
          })
        } else {
          this.success = "Already on the list"
        }
      })
      this.clearSuccess()
    },
    clearSuccess() {
      setTimeout(() => {
        this.email = "",
        this.success = ""
      }, 3000)
    }
  }
};
</script>

<style scoped>
</style>