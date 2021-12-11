<!--View-->
<template>
  <!--ROOT element-->
  <div>
    <h1>Hello</h1>
    <!--One-binding: from view to controller-->
    <input type="text" v-bind="name">
    <p>{{message}} {{name}}</p>
  </div>
</template>
<!--Controller-->
<script>
export default {
  /**
   * @data method used for returning data.
   * @returns {{name: string, message: string}}
   */
  data() {
    return {
      message: "Hello, ",
      name: "Unknown Name"
    }
  }
}
</script>

<!--Style-->
<style>
  body{
    background: green;
  }
</style>