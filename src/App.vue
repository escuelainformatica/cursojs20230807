<script setup>
import { ref } from 'vue'
import ListadoPaises from './components/ListadoPaises.vue';
import FormularioPais from './components/FormularioPais.vue';
// composicion
const variable = ref("hola mundo");
const paises = ref(["chile", "argentina", "peru"]);

</script>

<template>
  {{ variable }}
  <br>
  <ListadoPaises :valores="paises" />
  <FormularioPais :valores="paises"/>
  <ListadoPaises :valores="paises" />
  <ListadoPaises :valores="paises" />

</template>

<style scoped></style>
