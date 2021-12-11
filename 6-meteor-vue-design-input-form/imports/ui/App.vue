<template>
  <div>
    <form>
      <label for="firstName">First Name:</label>
      <input type="text" id="firstName" v-bind="firstName">
      <label for="lastName">Last Name:</label>
      <input type="text" id="lastName" v-bind="lastName">
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return{
      firstName: 'Chamrong',
      lastName: 'Thor'
    }
  }
}
</script>