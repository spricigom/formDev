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











    <div class="text-left">
        <div class="row">


            <div class="colLados text-center">

            </div>
            <div class="col">
                <div class="formulario">
                   
                    <div class="text-center">
                         <h1>Cadastre-se</h1>
                         <p>responda a esse formulário para criar sua conta</p>
                    </div>
                   
                    <hr style="margin-left:-10px; margin-right: -10px;">




                    <form @submit.prevent="enviarDados">

                        <div class="campo">
                            <label for="">Nome:</label>
                            <div class="linha">
                                <input type="text" class="form-control" v-model="perfil.nome"
                                    placeholder="Digite seu nome">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Email:</label>
                            <div class="linha">
                                <input type="email" class="form-control" v-model="perfil.email"
                                    placeholder="Digite seu email">
                            </div>
                        </div>


                      
                      
                      
                        <div class=" text-left">
                            <div class="row">
                                <div class="col">
                                    
                        <div class="campoEsq">
                            <label for="">Senha:</label>
                            <div class="linha">
                                <input type="password" class="form-control" v-model="perfil.senha"
                                    placeholder="Digite sua senha">
                            </div>
                        </div>
                                </div>
                                <div class="col">
                                     <div class="campoDir">
                            <label for="">Confirmação de Senha:</label>
                            <div class="linha">
                                <input type="password" class="form-control" v-model="perfil.confirmSenha"
                                    placeholder="Digite sua senha">
                            </div>
                        </div>
                                </div>
                                
                            </div>
                        </div>





                       

                        <div class="campo">
                            <label for="">Data de Nascimento:</label>
                            <div class="linha">
                                <input type="date" class="form-control" v-model="perfil.nascimento"
                                    placeholder="Data de Nascimento">
                            </div>
                        </div>


                        <div class="campo">
                            <label for="">Selecione seu Estado:</label>
                            <div class="linha">
                                <select name="estados" id="estados" class="form-control" v-model.lazy="estados.sigla">
                                    <option v-for="(item, index) in estados" :value="item" :key="index"> {{ item }}
                                    </option>
                                </select>
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Endereço:</label>
                            <div class="linha">
                                <input type="text" class="form-control" v-model="perfil.endereco"
                                    placeholder="Digite seu endereco">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Hobbies:</label>
                            <div class="linha">
                                <input type="text" class="form-control" v-model="perfil.hobbies"
                                    placeholder="Digite seus hobbies">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Linguagem de programação:</label>
                            <div class="linha">
                                <input type="text" class="form-control" v-model="perfil.linguagem"
                                    placeholder="Digite sua linguagem de programação">
                            </div>
                        </div>

                        <div class="campo">
                            <label for="">Biografia:</label>
                            <div class="linha">
                                <input type="text" class="form-control" v-model="perfil.biografia"
                                    placeholder="Digite sua biografia">
                            </div>
                        </div>




























                        <button type="submit" id="botao" class="btn btn-primary " style="margin-top: 25px; margin-left: 35px; margin-right: 35px; margin-bottom: 30px; width:90% ;"><h5>Mostrar</h5></button>
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
    width:27.5%;
    background-color: rgb(70, 70, 255);


}

.col {
    width: 45%;

}


.campo {
    margin-top: 10px;
    margin-bottom: 10px;
    margin-left: 35px;
    margin-right: 35px;
}
.campoEsq {
    margin-left: 35px;
}
.campoDir {
    margin-right: 35px;
}



.linha select,
input {
    width: 100%;
    height: 5vh;
    border-radius: 7px;
    background-color: rgb(231, 229, 229);
    border: .1px solid;
}
</style>