<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>Name</th>
          <th>Gender</th>
          <th>Age</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(user,index) in users" :key="index">
          <td>{{index}}</td>
          <td>{{user.name}}</td>
          <td>{{user.gender}}</td>
          <td>{{user.age}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          name: "Chamrong",
          gender: "M",
          age: 18,
        },
        {
          name: "Lam",
          gender: "F",
          age: 18,
        },
      ]
    }
  },
}
</script>