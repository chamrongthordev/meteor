<template>
  <div>
    <div id="userForm">
      <label for="firstName">នាមខ្លួន</label>
      <input type="text" id="firstName" v-model="firstName" />
      <br />
      <br />
      <label for="lastName">គោត្តនាម</label>
      <input type="text" id="lastName" v-model="lastName" />
      <br />
      <br />
      <label for="gender">ភេទ</label>
      <input type="text" id="gender" v-model="gender" />
      <br />
      <br />
      <label for="age">អាយុ</label>
      <input type="text" id="age" v-model="age" />
      <br />

      <button type="submit" @click="saveUser">ដាក់ស្នើ</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      gender: "",
      age: "",
    }
  },

  methods: {
    saveUser() {
      alert(`
      ឈ្មោះ៖ ${this.lastName} ${this.firstName}
      ភេទ៖ ${this.gender}
      អាយុ៖ ${this.age}
      `)
    }
  },
}
</script>

<style>
body {
  font-family: 'hanuman', sans-serif;
}
</style>
