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
        <tr v-for='(user, index) in users' :key='index'>
          <td v-if="user.gender=='M'">{{index}}</td>
          <td v-if="user.gender=='M'">{{user.name}}</td>
          <td v-if="user.gender=='M'">{{user.gender}}</td>
          <td v-if="user.gender=='M'">{{user.age}}</td>
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
          age: 21
        },
        {
          name: "Lam",
          gender: "F",
          age: 21
        }
      ]
    }
  },
}
</script>