<template>
  <div class="login-container">
    <form class="login-form">
      <h2>Login</h2>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" v-model="password" required />
      </div>
      <button type="submit" @click.prevent="login">Sign In</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const email = ref('');
const password = ref('');

function login() {
  // Add login logic here
  alert(`Email: ${email.value}\nPassword: ${password.value}`);
}
</script>

<style scoped>
.login-container {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #fff;
}
.login-form {
  background: #fff;
  padding: 2rem 2.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 16px rgba(0,0,0,0.08);
  width: 100%;
  max-width: 350px;
  display: flex;
  flex-direction: column;
}
.login-form h2 {
  margin-bottom: 1.5rem;
  text-align: center;
}
.form-group {
  margin-bottom: 1rem;
  display: flex;
  flex-direction: column;
}
.form-group label {
  margin-bottom: 0.5rem;
  font-weight: 500;
}
.form-group input {
  padding: 0.5rem;
  border: 1px solid #ddd;
  border-radius: 6px;
  font-size: 1rem;
}
button[type="submit"] {
  background: #42b983;
  color: #fff;
  border: none;
  border-radius: 6px;
  padding: 0.75rem;
  font-size: 1rem;
  cursor: pointer;
  margin-top: 1rem;
  transition: background 0.2s;
}
button[type="submit"]:hover {
  background: #369870;
}
</style>
