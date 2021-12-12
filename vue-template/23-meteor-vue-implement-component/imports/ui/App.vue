<template>
  <div>
    <component-signup @handleSignUp="handleSignUp" />
  <component-table :usersData="datas"/>
  </div>
</template>

<script>
import ComponentSignup from './components/ComponentSignup.vue'
import ComponentTable from './components/ComponentTable.vue'

export default {
  components: { ComponentSignup, ComponentTable },
  data() {
    return {
      datas: [],
    }
  },
  methods: {
    handleSignUp(res) {
      this.datas.push(res)
    },
  },
}
</script>

<style></style>
