<template>

    <div>
        <h1>Ola Vue!</h1>
        <p>Meu nome é {{ nome }} e tenho {{ age }} anos</p>
        <MultiplosEventos />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
    </div>

</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue'
    import Reutilizacao from './Reutilizacao.vue';
    export default{
        name: 'PrimeiroComponent',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return{
                nome:"luis", 
                age: 28
            }
        }
    }
</script>