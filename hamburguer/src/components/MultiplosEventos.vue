<template>
    <div>
        <button @click="primeiro(txt1, $evento), segundo(txt2, $evento), terceiro($evento)"> Ativar!!</button>
        <p> {{ multiplosEventos }}</p>
    </div>
</template>

<script>
    export default{
        name: 'MultiplosEventos',
        data(){
            return{
                multiplosEventos: '',
                txt1: "primeiro Evento",
                txt2: "segundo evento"
            }
        },
        methods:{
            primeiro(txt, e){
                this.multiplosEventos = txt
            },
            segundo(txt, e){
                setTimeout(()=> this.multiplosEventos = txt, 500)
            },
            terceiro(e){
                setTimeout(()=> this.multiplosEventos = "", 1000)
            }
        }
    }
</script>

<style scoped>
    div{
        margin: 100px;
    }
</style>