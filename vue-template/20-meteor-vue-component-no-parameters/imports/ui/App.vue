<template>
  <div>
    <chamrong/>
  </div>
</template>

<script>
import Hello from './components/Hello.vue'
import Info from './components/Info.vue'
import Chamrong from './components/Chamrong.vue'

export default {
  components: {
    Hello,
    Info,
    Chamrong
  },
}
</script>

<style>
  body {
    font-family: sans-serif;
    padding: 10px;
  }
</style>
