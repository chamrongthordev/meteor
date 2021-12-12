<template>
  <div>
    <button @click="handleUpdate">Update Name</button>
    My name is : {{ name }}

    <info v-if="active"/>
  </div>
</template>

<script>
import Info from './components/Info.vue'
export default {
  components: {
    Info,
  },

  data() {
    return {
      name: 'Chamrong',
      active: true,
    }
  },

  methods: {
    handleUpdate() {
      this.name = 'Thor Chamrong';
      this.active = false;
    },
  },

  beforeCreate() {
    console.log('beforeCreate')
  },

  created() {
    console.log('created')
  },

  beforeMount() {
    console.log('beforeMount')
  },

  mounted() {
    console.log('mounted')
  },

  beforeUpdate() {
    console.log('beforeUpdate')
  },

  updated() {
    console.log('updated')
  },

  beforeDestroy() {
    console.log('beforeDestroy')
  },

  destroyed() {
    console.log('destroyed')
  },
}
</script>
