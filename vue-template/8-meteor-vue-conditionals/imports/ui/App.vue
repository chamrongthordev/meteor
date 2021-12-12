<template>
  <div>
    <p v-if="condition1">I'm condition 1</p>
    <p v-else-if="condition2">I'm condition 2</p>
    <p v-else>I'm condition 3</p>
  </div>
</template>

<script>

export default {
  data() {
    return {
      condition1: true,
      condition2: true,
      condition3: false
    }
  },
}
</script>

<style>
  body {
    font-family: sans-serif;
    padding: 10px;
  }
</style>
