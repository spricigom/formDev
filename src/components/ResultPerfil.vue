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
                <div class="campo">
                            <label for="">Nome:</label>
                            <div class="linha">
                                <p>{{ perfil.nome }}</p>
                            </div>
                        </div>

              


                <label for="">Email:</label>
                <p>{{ perfil.email }}</p>

                <label for="">Senha:</label>
                <p>{{ perfil.senha }}</p>

                <label for="">Data de Nacimento:</label>
                <p>{{ perfil.nascimento }}</p>

                <label for="">Estado:</label>
                <p>{{ perfil.estados }}</p>

                <label for="">Cidade:</label>
                <p>{{ perfil.cidade }}</p>

                <label for="">Endereço:</label>
                <p>{{ perfil.endereco }}</p>

                <label for="">Hobbies:</label>
                <p>{{ perfil.hobbies }}</p>

                <label for="">Linguagem de Programação:</label>
                <p>{{ perfil.linguagem }}</p>
                
                <label for="">Biografia:</label>
                <p>{{ perfil.biografia }}</p>

            </div>
            <div class="colLados text-center">

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
}

.cima {
    background-color: rgb(70, 70, 255);
    height: 100px;
}

.campo {
    margin-top: 10px;
    margin-bottom: 10px;
    margin-left: 35px;
    margin-right: 35px;
}
</style>