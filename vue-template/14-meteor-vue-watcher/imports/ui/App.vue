<template>
  <div>
    <input type="text" name="firstName" id="firstName" v-model="firstName">
    <input type="text" name="lastName" id="lastName" v-model="lastName">
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

  watch: {
    firstName: value => console.log(`firstName: ${value}`),
    lastName: value=> console.log(`lastName: ${value}`)
  }
}
</script>