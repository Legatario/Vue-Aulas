<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>

    export default{
        name: 'LyfeCycle',
        data(){
            return{
                nome: 'ainda não sei'
            }
        },
        created(){
            setTimeout(() =>{
                this.nome = 'Luis'
            },1000)
            this.lifeCycle()
        },
        mounted(){
            setTimeout(() =>{
                this.nome = 'Phillipe'
            },2000)
        },
        methods:{
            lifeCycle(){
                console.log("executou")
            }
        }
    }
</script>