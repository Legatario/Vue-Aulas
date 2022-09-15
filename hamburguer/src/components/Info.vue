<template>
    <div>
        <p>{{ email }}</p>
        <p v-if="esta_trabalahndo">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Ultilizo as seguintes tecnologias</p>
        <ul>
            <li v-for="(tec, index) in tecnologias" v-bind:key="index" >{{ tec }}</li>
        </ul>
        <p>Ultilizo as seguintes frameworks</p>
        <ul>
            <li v-for="tec in frameworks" :key="tec.id">{{ tec.language }}</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoButton }}</button>
        </div>
        <p v-show="mostrar_email" class="teste">Mande uma mensagem para {{ email }}</p>
        <p>Para acessar meu portifolio basta <a v-bind:href="meu_link" target="_bank">clicar aqui </a></p>
        <Imgs />
    </div>    
</template>

<script>
import Imgs from './imgs.vue';
    export default{
    nome: "Info",
    data() {
        return {
            esta_trabalahndo: true,
            mostrar_email: false,
            meu_link: "https://google.com",
            textoButton : 'Mostrar E-mail',
            tecnologias: ['Javascript','HTML','CSS'],
            frameworks: [
                {id: 1, language: 'React'},
                {id: 2, language: 'Angular'},
                {id: 3, language: 'Vue'}
            ]
        };
    },
    components: { 
        Imgs 
    },
    methods:{
        showEmail(){
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
                this.textoButton = 'Mostar e-mail'
            } else{
                this.textoButton = 'Ocultar e-mail'
            }
        }
    },
    props:{
        email: String,
        esta_trabalahndo: Boolean
    }
}
</script>