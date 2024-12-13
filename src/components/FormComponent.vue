<template>
    <div class="form-container">
    <h1>📝 Formulário</h1>
      <input v-model="nome" placeholder="Digite seu nome..." />
      <input v-model="email" placeholder="Digite seu email..." />
      <button @click="enviarDados">Enviar</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        nome: '',
        email: '',
      };
    },
    methods: {
      enviarDados() {
        this.$emit('enviar-dados', { nome: this.nome, email: this.email });
        this.nome = '';
        this.email = '';
      },
    },
  };
  </script>
  
  <style>
  .form-container {
    padding: 20px;
    background-color: #118B50;
    display: flex;
    flex-direction: column; 
    align-items: center; 
    justify-content: center; 
    margin: 1px;
  }
  
  input {
    margin: 10px 0; 
    padding: 8px;
    width: 200px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    padding: 8px 12px;
    background-color: #d7590a;
    color: rgb(0, 0, 0);
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  button:hover {
    background-color: #ffffff;
  }
  </style>
  