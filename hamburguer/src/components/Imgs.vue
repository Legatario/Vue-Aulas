<template>
    <div>
        <img :src="avatar" :alt="alt">
        <MudarImagem @mudar-imagem="trocarImagem" />
    </div>
</template>

<script>
import MudarImagem from './MudarImagem.vue';
    export default{
    name: "Imgs",
    data() {
        return {
            avatar: "/image/avatar.png",
            alt: "Luis Phillipe"
        }
    },
    components: { 
        MudarImagem 
    },
    methods:{
        trocarImagem(){
            this.avatar = '/image/avatar2.png'
        }
    }

}
</script>