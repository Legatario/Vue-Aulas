<template>
    <form action="" @submit="enviarFormulario">
        <h2>Meu Formulario</h2>
        <div>
            <input type="text" v-model="name">
        </div>
        <div>
            <input type="text" v-model="email">
        </div>
        <div>
            <Submit />
        </div>
    </form>
</template>


<script>
    import InputText from './InputText.vue';
    import Submit from './Submit.vue';
        export default{
        nome: 'Form',
        components:{
            InputText,
            Submit
        },
        methods:{
            enviarFormulario(e){
                e.preventDefault();
                const name = this.name;
                const email = this.email;

                console.log("formulario enviado")
                console.log("O nome é: " +name)
                console.log("O email é: " +email)
            }
        },
        data(){
            return{
                name: "",
                email: ""
            }
        } 
    }
</script>
