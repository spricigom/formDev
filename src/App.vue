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

function salvarPerfil(novoPerfil) {
    Object.assign(perfil, novoPerfil)
}
</script>

<template>
 <EditPerfil @enviarAlteracoes="salvarPerfil"/>
 <ResultPerfil :perfil="perfil"/>
</template>

<style scoped>

</style>
