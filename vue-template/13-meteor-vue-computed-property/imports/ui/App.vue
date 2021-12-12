<template>
  <div>
    <input type="text" name="fistName" id="firstName" v-model="firstName">
    <input type="text" name="lastName" id="lastName" v-model="lastName">

    <div id="showName">
      My name is {{fullName}}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: ""
    }
  },

  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    }
  }
}
</script>