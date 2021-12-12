<template>
  <div>
    <div id="tableUser">
      <table border="2">
        <thead>
          <tr>
            <th>ID</th>
            <th>Username</th>
            <th>Password</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(user, index) in usersData" :key="index">
            <td>{{ index }}</td>
            <td>{{ user.username }}</td>
            <td>{{ user.password }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    usersData: {
      type: Array,
      default: [],
    },
  },
}
</script>
