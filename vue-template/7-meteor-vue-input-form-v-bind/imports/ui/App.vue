<template>
  <div>
    <!-- v-model -->
    <input type="text" name="firstName" id="firstName" v-model="firstName">
    <input type="text" name="lastName" id="lastName" v-model="lastName">
    <!-- v-bind -->
    <input type="text" name="firstName" id="fistName" v-bind:value="firstName">
    <input type="text" name="lastName" id="lastName" v-bind:value="lastName">
  </div>
</template>

<script>

export default {
  data() {
    return {
      firstName: 'Chamrong',
      lastName: 'Thor'
    }
  }
}
</script>