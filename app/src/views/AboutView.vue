<template>
  <div>
    <NewList />
    <form action="submit" @submit.prevent="login(user)">
      <label for="username">Username</label>
      <input type="text" v-model="user.username"/>
      <label for="password">Password</label>
      <input type="password" v-model="user.password"/>
      <button>Login</button>
    </form>
    <h2 v-if="loggedIn">Hello Peter</h2>
    <h2 v-else>Please Login</h2>
  </div>
</template>

<script setup>
import NewList from "../components/NewList.vue"
import { reactive } from  "vue"
const user = reactive({username: '', password: ''})
function login(user){
  console.log(user)
}
</script>

<style scoped></style>