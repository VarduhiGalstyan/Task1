<template>
    <div class="page">
      <h2 >Register</h2>
      <form @submit.prevent="handleSubmit">
        <div>
          <label for="username">Username:</label>
          <input type="text" id="username" v-model="formData.username" required />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="formData.email" required />
        </div>
        <div>
          <label for="password">Password:</label>
          <input type="password" id="password" v-model="formData.password" required />
        </div>
        <div>
          <button type="text" >Save</button>
        </div>
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const formData = ref({
    username: '',
    email: '',
    password: ''
  });
  
  const handleSubmit = () => {
    console.log(' New account:', formData.value);
  };
  </script>
  
  <style scoped>
  .page{
    padding: 5px 30% 5px 30%;
    width: 40%;
  }
  h2{
    background-color: #4dba05;
  }
  form {
    display: flex;
    flex-direction: column;
  }
  
  label {
    margin-bottom: 5px;
  }
  
  input {
    margin-bottom: 15px;
    padding: 8px;
    border: 1px solid #2eed58;
    border-radius: 4px;
  }
  </style>