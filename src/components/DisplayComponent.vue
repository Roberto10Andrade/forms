<template>
    <div>
      <p v-if="dados.nome">Nome: {{ dados.nome }}</p>
      <p v-if="dados.email">Email: {{ dados.email }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['dados'],
  };
  </script>
  
  <style>
  p {
    font-size: 16px;
    position: center;
  }
  </style>
  