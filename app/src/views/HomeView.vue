<!-- <template>
  <div>
    <form @submit.prevent>
      <p>Username</p>
      <input type="text" v-model="user.username" required>
      <p>Password</p>
      <input type="text" v-model="user.password" required>
      <button type="submit" @click="getData">Login</button>
    </form>
  </div>
</template>

<script setup>
/* import {ref, reactive} from 'vue'
const count = ref(0)
const user = ref('')
function increment(){
  count.value++
} */
</script>
 
<style scoped></style> -->

<script setup>
  import LogIn from '../components/LogIn.vue';
</script>

<template>
  <main>
    <Login message="Hello World" :count = "5"><h1>Hello Laith</h1></Login>
  </main>
</template>