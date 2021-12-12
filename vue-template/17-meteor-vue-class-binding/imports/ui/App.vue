<template>
  <div>
    <p :class="{'static-paragraph': active}">I'm a red paragraph</p>
    <button @click="handleActiveParagraph">Modified Paragraph style</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: true
    }
  },

  methods: {
    handleActiveParagraph() {
      this.active = !this.active;
    }
  },
}
</script>

<style>
  .static-paragraph {
    color: green;
  }

  .inactive-paragraph {
    color: gray;
  }
</style>