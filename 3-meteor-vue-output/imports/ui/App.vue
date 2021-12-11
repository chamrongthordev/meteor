<!--View-->
<template>
  <!--ROOT element-->
  <div>
    <h1>{{ message }}</h1>
    <p>
      Hello, {{ name }}
    </p>
  </div>
</template>

<!--Controller-->
<script>

export default {
  data() {
    return {
      message: "Hello, Vue",
      name: "Chamrong"
    }
  }
}
</script>

<!--Style-->
<style>
body {
  font-family: sans-serif;
  padding: 10px;
}
</style>
