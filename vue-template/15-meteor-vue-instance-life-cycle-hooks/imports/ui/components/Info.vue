<template>
  <div>
    <h4>This is a compunents.</h4>
  </div>
</template>

<script>
export default {
  beforeDestroy() {
    console.log("beforeDestroy");
  },

  destroyed() {
    console.log("destroyed");
  },
}
</script>