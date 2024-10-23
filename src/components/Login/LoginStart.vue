<template>
    <div class="login-container">
      <div class="login-box">
        <h2>Login</h2>
        <form @submit.prevent="login">
          <div class="input-box">
            <input
              type="text"
              v-model="email"
              required
              placeholder="email"
            />
          </div>
          <div class="input-box">
            <input
              type="password"
              v-model="password"
              required
              placeholder="Password"
            />
          </div>
          <button type="submit" class="btn-login">Log In</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const username = ref('');
      const password = ref('');
  
      const login = () => {
        alert(`Usuário: ${username.value} Senha: ${password.value}`);
      };
  
      return {
        username,
        password,
        login,
      };
    },
  };
  </script>
  
  <style scoped>
  .login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
  }
  
  .login-box {
    background-color: #fff;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 300px;
  }
  
  h2 {
    margin-bottom: 20px;
    color: #333;
  }
  
  .input-box {
    margin-bottom: 20px;
  }
  
  .input-box input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 16px;
  }
  
  .input-box input:focus {
    border-color: #5b9bd5;
    outline: none;
  }
  
  .btn-login {
    width: 100%;
    padding: 10px;
    background-color: #5b9bd5;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
  }
  
  .btn-login:hover {
    background-color: #4a8dc5;
  }
  </style>
  