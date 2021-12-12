<template>
  <div>
    <div id="signUpForm">
      <h5>Component Sign Up</h5>
      <label for="username">Username:</label>
      <input type="text" id="username" v-model="username" />
      <br />
      <label for="password">Password</label>
      <input type="text" id="password" v-model="password" />

      <button @click="handleSignUp">Sign Up</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
      datas: {},
    }
  },

  methods: {
    handleSignUp() {
      this.datas = {
        username: this.username,
        password: this.password,
      }
      this.$emit('handleSignUp', this.datas)
    },
  },
}
</script>

<style></style>
