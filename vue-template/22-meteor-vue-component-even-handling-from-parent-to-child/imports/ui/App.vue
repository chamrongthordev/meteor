<template>
  <div>
    <chamrong @iLoveU="handleClicks"/>
  </div>
</template>

<script>
import Chamrong from './components/Chamrong.vue'
export default {
  components: {
    Chamrong,
  },

  methods: {
    handleClicks(name) {
      alert(`'I LOVE ${name}!'`);
    },
  },
}
</script>
