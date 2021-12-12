<template>
  <button @click="handleValue">Hello, World</button>
</template>

<script>
export default {
    methods: {
        handleValue() {
            console.log(this.$emit('iLoveU', 'Chamrong'));
        }
    },
}
</script>