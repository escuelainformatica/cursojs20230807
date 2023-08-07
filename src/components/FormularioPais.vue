<script setup>
import { ref } from 'vue';
const propiedades=  defineProps(['valores']); // reactivas (no necesito ocupar .value)
const searchText = ref(""); // referencias (pero necesito ocupar .value para asignarles valores)
function cambiarTexto() {
    searchText.value = "";
}
function boton() {
    // variable="hello world"; // la variable ya no es una referencia, es solo un texto
    //variable.value = "hello world"; // la variable sigue siendo una referencia, lo que cambio es el valor
    //console.log(variable);
    console.log(propiedades.valores);
    propiedades.valores.push(searchText.value);
    searchText.value = "";
}

</script>
<template>
    <br>
    <input type="text" id="campo1" v-model="searchText" />
    <button v-on:click="cambiarTexto">Limpiar</button>
    <br>
    <button v-on:click="boton">haga click aqui</button>
</template>