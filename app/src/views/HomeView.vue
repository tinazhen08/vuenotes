<template>
  <div>
    <form>
      <p>Username</p>
      <input type="text" v-model="username" required>
      <p>Password</p>
      <input type="text" v-model="password" required>
      <button type="submit">Login</button>
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

import { reactive } from "vue";

const user = reactive({
  username: '',
  password: ''
})

function getData(){
  
}
</script>
 
<style scoped></style>