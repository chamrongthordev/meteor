<template>
  <div>
    <button v-on:click="sayHello">Say Hello</button>
  </div>
</template>

<script>
export default {
  methods: {
    sayHello() {
      alert("Hello");
    }
  },
}
</script>