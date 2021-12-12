<template>
  <div>
    <div id="userForm">
      <label for="username">Username:</label>
      <input type="text" id="username" v-model="username" />
      <br />
      <label for="password">Password:</label>
      <input type="text" id="password" v-model="password" />
      <label for="gender">Gender</label>
      <input
        type="radio"
        name="gender"
        id="gender"
        value="Male"
        v-model="gender"
      />
      <input
        type="radio"
        name="gender"
        id="gender"
        value="Female"
        v-model="gender"
      />
      <label for="habit">Habit</label>
      <input
        type="checkbox"
        name="habit"
        id="habit"
        value="Reading"
        v-model="habits"
      />
      <input
        type="checkbox"
        name="habit"
        id="habit"
        value="Learning"
        v-model="habits"
      />
      <input
        type="checkbox"
        name="habit"
        id="habit"
        value="Singing"
        v-model="habits"
      />
    </div>

    <div id="tableUser">
      <table border="2">
        <thead>
          <tr>
            <th>ID</th>
            <th>Username</th>
            <th>Gender</th>
            <th>Habits</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(user, index) in users" :key="index">
            <td>{{index +1}}</td>
            <td>{{user.username}}</td>
            <td>{{user.gender}}</td>
            <td>{{user.habits}}</td>
          </tr>
        </tbody>
      </table>
    </div>

    <button @click="saveUser">Save User</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
      gender: '',
      habits: [],
      users: [{}],
    }
  },

  methods: {
    saveUser() {
      this.users.push({
        username: this.username,
        password: this.password,
        gender: this.gender,
        habits: this.habits,
      });
    },
  },
}
</script>
