<script setup>
import { reactive, ref } from 'vue';
const emit = defineEmits(['enviarAlteracoes'])
const estados = [{
    nome: 'Acre',
    sigla: 'AC'
},
{
    nome: 'Alagoas',
    sigla: 'AL'
},
{
    nome: 'Amapá',
        sigla: 'AP'
},
{
    nome: 'Amazonas',
    sigla: 'AM'
},
{
    nome: 'Bahia',
    sigla: 'BA'
},
{
    nome: 'Ceará',
    sigla: 'CE'
},
{
    nome: 'Distrito Federal',
    sigla: 'DF'
},
{
    nome: 'Espírito Santo',
    sigla: 'ES'
},
{
    nome: 'Goiás',
    sigla: 'GO'
},
{
    nome: 'Maranhão',
    sigla: 'MA'
},
{
    nome: 'Mato Grosso',
    sigla: 'MT'
},
{
    nome: 'Minas Gerais',
    sigla: 'MG'
},
{
    nome: 'Mato Grosso do Sul',
    sigla: 'MS'
},
{
    nome: 'Pará',
    sigla: 'PA'
},
{
    nome: 'Paraíba',
    sigla: 'PB'
},
{
    nome: 'Pernambuco',
    sigla: 'PE'
},
{
    nome: 'Piauí',
    sigla: 'PI'
},
{
    nome: 'Rio de Janeiro',
    sigla: 'RJ'
},
{
    nome: 'Rio Grande do Norte',
    sigla: 'RN'
},
{
    nome: 'Rio Grande do Sul',
    sigla: 'RS'
},
{
    nome: 'Rondônia',
    sigla: 'RO'
},
{
    nome: 'Roraima',
    sigla: 'RR'
},
{
    nome: 'Santa Catarina',
    sigla: 'SC'
},
{
    nome: 'São Paulo',
    sigla: 'SP'
},
{
    nome: 'Sergipe',
    sigla: 'SE'
},
{
    nome: 'Tocantins',
    sigla: 'TO'
}
];

const perfil = reactive({
    nome: '',
    email: '',
    senha: '',
    confirmSenha: '',
    nascimento: '',
    endereco: '',
    hobbies: '',
    linguagem: '',
    biografia: ''
})

function enviarDados() {
    let error = false
    // if (perfil.nome == '') {
    //     alert("Faltou o nome")
    //     error = true
    // }
    // if (perfil.email == '') {
    //     alert("Faltou o email")
    //     error = true
    // }
    // if (perfil.senha == '') {
    //     alert("Faltou a senha")
    //     error = true
    // }
    // if (perfil.confirmSenha == '') {
    //     alert("Faltou a confirmação de senha")
    //     error = true
    // }
    // if (perfil.senha !== perfil.confirmSenha) {
    //     alert("Senhas não conferem")
    //     error = true
    // }
    // if (perfil.nascimento == '') {
    //     alert("Faltou a data de nascimento")
    //     error = true
    // }
    // if (perfil.endereco == '') {
    //     alert("Faltou o endereço")
    //     error = true
    // }
    // if (perfil.hobbies == '') {
    //     alert("Faltou o hobbies")
    //     error = true
    // }
    // if (perfil.linguagem == '') {
    //     alert("Faltou a linguagem de programção")
    //     error = true
    // }
    // if (perfil.biografia == '') {
    //     alert("Faltou a sua biografia")
    //     error = true
    // }
    // if (perfil.estado == '') {
    //     alert("Faltou o estado")
    //     error = true
    // }
    // validar
    if (!error) {
        // mostrarResultado.value = !mostrarResultado.value
        emit('enviarAlteracoes', { ...perfil })
    }
}
</script>
<template>
    <form @submit.prevent="enviarDados">
        <h1>Formulário</h1>
        <label for="">Nome:</label>
        <input type="text" v-model="perfil.nome" placeholder="Digite seu nome">
        <label for="">Email:</label>
        <input type="email" v-model="perfil.email" placeholder="Digite seu email">
        <label for="">Senha:</label>
        <input type="password" v-model="perfil.senha" placeholder="Digite sua senha">
        <label for="">Confirmação de Senha:</label>
        <input type="password" v-model="perfil.confirmSenha" placeholder="Digite sua senha">
        <label for="">Data de Nascimento:</label>
        <input type="date" v-model="perfil.nascimento" placeholder="Data de Nascimento">
        <label for="">Selecione seu Estado:</label>
        <select name="estados" id="estados" v-model.lazy="estados.sigla">
            <option v-for="(item, index) in estados" :value="item" :key="index"> {{ item }}</option>
        </select>
        <label for="">Endereço:</label>
        <input type="text" v-model="perfil.endereco" placeholder="Digite seu endereco">
        <label for="">Hobbies:</label>
        <input type="text" v-model="perfil.hobbies" placeholder="Digite seus hobbies">
        <label for="">Linguagem de programação:</label>
        <input type="text" v-model="perfil.linguagem" placeholder="Digite sua linguagem de programação">
        <label for="">Biografia:</label>
        <input type="text" v-model="perfil.biografia" placeholder="Digite sua biografia">
        <button type="submit" id="botao" class="btn">Mostrar</button>
    </form>
</template>