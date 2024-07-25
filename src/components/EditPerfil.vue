<script setup>
import { reactive } from 'vue';
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
    <h1>Formulário</h1>






    <form>
        <div class="mb-3">
            <label for="exampleInputEmail1" class="form-label">Email address</label>
            <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
            <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
        </div>
        <div class="mb-3">
            <label for="exampleInputPassword1" class="form-label">Password</label>
            <input type="password" class="form-control" id="exampleInputPassword1">
        </div>
        <div class="mb-3 form-check">
            <input type="checkbox" class="form-check-input" id="exampleCheck1">
            <label class="form-check-label" for="exampleCheck1">Check me out</label>
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
    </form>



    <div class="container text-left">
        <div class="row">


            <div class="colLados text-center">

            </div>
            <div class="col">
                <div class="formulario">
                    <form @submit.prevent="enviarDados">

                        <div class="campo">
                            <label for="">Nome:</label>
                            <div class="linha">
                                <input type="text" v-model="perfil.nome" placeholder="Digite seu nome">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Email:</label>
                            <div class="linha">
                                <input type="email" v-model="perfil.email" placeholder="Digite seu email">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Senha:</label>
                            <div class="linha">
                                <input type="password" v-model="perfil.senha" placeholder="Digite sua senha">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Confirmação de Senha:</label>
                            <div class="linha">
                                <input type="password" v-model="perfil.confirmSenha" placeholder="Digite sua senha">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Data de Nascimento:</label>
                            <div class="linha">
                                <input type="date" v-model="perfil.nascimento" placeholder="Data de Nascimento">
                            </div>
                        </div>


                        <div class="campo">
                            <label for="">Selecione seu Estado:</label>
                            <div class="linha">
                                <select name="estados" id="estados" v-model.lazy="estados.sigla">
                                    <option v-for="(item, index) in estados" :value="item" :key="index"> {{ item }}
                                    </option>
                                </select>
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Endereço:</label>
                            <div class="linha">
                                <input type="text" v-model="perfil.endereco" placeholder="Digite seu endereco">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Hobbies:</label>
                            <div class="linha">
                                <input type="text" v-model="perfil.hobbies" placeholder="Digite seus hobbies">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Linguagem de programação:</label>
                            <div class="linha">
                                <input type="text" v-model="perfil.linguagem"
                                    placeholder="Digite sua linguagem de programação">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Biografia:</label>
                            <div class="linha">
                                <input type="text" v-model="perfil.biografia" placeholder="Digite sua biografia">
                            </div>
                        </div>




























                        <button type="submit" id="botao" class="btn btn-primary">Mostrar</button>
                    </form>
                </div>
            </div>
            <div class="colLados text-center">

            </div>
        </div>
    </div>

</template>






<style scoped>
.colLados {
    width: 30%;

}

.col {
    width: 40%;

}


.campo {
    margin-top: 15px;
    margin-bottom: 15px;
}

.linha select,
input {
    width: 100%;
    height: 4vh;
    border-radius: 10px;
}
</style>