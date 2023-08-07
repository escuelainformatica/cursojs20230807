<script setup>
    const propiedades=defineProps(['valores']);
</script>
<template>
  <ul>
    <li v-for="pais in propiedades.valores" v-bind:key="pais.value">{{ pais }}</li>
  </ul>
</template>