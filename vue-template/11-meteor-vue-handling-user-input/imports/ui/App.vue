<template>
  <div>
    <!-- <button v-on:click="sayHello">Say Hello</button> -->
    <button @click="sayHello">Say Hello</button>
    
    <!-- <button v-on:keyup="goodBy">Say Hello</button> -->
    <input type="text" name="firstName" id="firstName" @keyup.enter="goodBy">

    <p :title="`I love you`">dd</p>
  </div>
</template>

<script>
export default {
  methods: {
    sayHello() {
      alert("Hello");
    },

    goodBy() {
      alert("Good by")
    }
  },
}
</script>