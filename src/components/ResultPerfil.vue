<script setup>
defineProps(['perfil'])
</script>

<template>
    <div class="cima text-center">
        <div class="row">
            <div class="col">

            </div>
            <div class="col">

            </div>
            <div class="col">

            </div>
        </div>
    </div>


    <div class="text-left ">
        <div class="row">
            <div class="colLados text-center">
            </div>
            <div class="col">

                <div class="titulo text-center">
                    <h1>Resultados</h1> 
                    <p>Confira aqui os dados do seu cadastro</p>
                    <hr style="margin-left:-10px; margin-right: -10px;">
                   
                </div>
                <div class="campo">

                    <label for="">Nome:</label>
                    <div class="linha">
                        <h3>{{ perfil.nome }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Email:</label>
                    <div class="linha">
                        <h3>{{ perfil.email }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Senha:</label>
                    <div class="linha">
                        <h3>{{ perfil.senha }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Data de Nacimento:</label>
                    <div class="linha">
                        <h3>{{ perfil.nascimento }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Estado:</label>
                    <div class="linha">
                        <h3>{{ perfil.estados }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Cidade:</label>
                    <div class="linha">
                        <h3>{{ perfil.cidade }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Endereço:</label>
                    <div class="linha">
                        <h3>{{ perfil.endereco }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Hobbies:</label>
                    <div class="linha">
                        <h3>{{ perfil.hobbies }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Hobbies:</label>
                    <div class="linha">
                        <h3>{{ perfil.hobbies }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Linguagem de Programação:</label>
                    <div class="linha">
                        <h3>{{ perfil.linguagem }}</h3>
                    </div>
                </div>

                <div class="campo">
                    <label for="">Biografia:</label>
                    <div class="linha">
                        <h3>{{ perfil.biografia }}</h3>
                    </div>
                </div>












            </div>
            <div class="colLados text-center">

            </div>
        </div>
    </div>

    <div class="cima text-center">
        <div class="row">
            <div class="col">

            </div>
            <div class="col">

            </div>
            <div class="col">

            </div>
        </div>
    </div>


</template>

<style scoped>
.colLados {
    width: 27.5%;
    background-color: rgb(70, 70, 255);


}

.col {
    width: 45%;
    margin-bottom: 30px;
}

.cima {
    background-color: rgb(70, 70, 255);
    height: 100px;
}

.campo {
    margin-top: 20px;
    margin-bottom: 20px;
    margin-left: 35px;
    margin-right: 35px;
}
.titulo{
    margin-top: 50px;
}
</style>