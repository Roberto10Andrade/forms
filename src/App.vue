<template>
  <div id="app">
    <FormComponent @enviar-dados="atualizarDados" />
    <DisplayComponent :dados="dadosFormulario" />
  </div>
</template>

<script>
import FormComponent from './components/FormComponent.vue';
import DisplayComponent from './components/DisplayComponent.vue';

export default {
  components: {
    FormComponent,
    DisplayComponent,
  },
  data() {
    return {
      dadosFormulario: {},
    };
  },
  methods: {
    atualizarDados(dados) {
      this.dadosFormulario = dados;
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  margin: 20px;
}
</style>
