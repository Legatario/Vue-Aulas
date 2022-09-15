<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        <Info :email="email" :esta_trabalahndo=true />
    </div>
</template>

<script>
import Info from './Info.vue';
    export default{
    nome: "Pessoa",
    data() {
        return {
            nome: "Guilherme",
            email: "lulu@gmail.com"
        };
    },
    components: { Info }
}
</script>