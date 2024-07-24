<script setup>
import { reactive } from 'vue';
import ResultPerfil from './components/ResultPerfil.vue';
import EditPerfil from './components/EditPerfil.vue';

const perfil = reactive({
    nome: '',
    email: '',
    senha: '',
    confirmSenha: '',
    nascimento: '',
    endereco: '',
    estado: '',
    hobbies: '',
    linguagem: '',
    biografia: ''
})
</script>

<template>
 <EditPerfil :perfil="perfil" @mostrarPerfil="perfil"/>
 <ResultPerfil :mostrarPerfil="perfil"/>
</template>

<style scoped>

</style>
