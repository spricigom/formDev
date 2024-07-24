<script setup>
defineProps(['perfil'])
</script>

<template>
    <label for="">Nome:</label>
    <p>{{ perfil.nome }}</p>
    <label for="">Email:</label>
    <p>{{ perfil.email }}</p>
    <label for="">Senha:</label>
    <p>{{ perfil.senha }}</p>
    <label for="">Data de Nacimento:</label>
    <p>{{ perfil.nascimento }}</p>
    <label for="">Endereço:</label>
    <p>{{ perfil.endereco }}</p>
    <label for="">Hobbies:</label>
    <p>{{ perfil.hobbies }}</p>
    <label for="">Linguagem de Programação:</label>
    <p>{{ perfil.linguagem }}</p>
    <label for="">Biografia:</label>
    <p>{{ perfil.biografia }}</p>
</template>

<style scoped>
</style>