<template>
  <div>
    <Header :esta_logado="true" />
    <PrimeiroComponent />
    <p>O nome do app é: {{ testando }}</p>
    <LifeCycleVue />
    <Pessoa />
    <Form />
  </div>
</template>

<script>
  import PrimeiroComponent from './components/PrimeiroComponent.vue';
  import LifeCycleVue from './components/LifeCycle.vue';
  import Pessoa from './components/Pessoa.vue';
  import Form from './components/Form/Form.vue';
  import Header from './components/Header.vue';

  export default{
    name: 'App',
    components:{
    PrimeiroComponent,
    LifeCycleVue,
    Pessoa,
    Form,
    Header
},
    data(){
      return{
        testando: "Teste"
      }
    }
  }
</script>

<style>
  body{
    color: #fff;
    background: #333;
  }

  a{
    color: greenyellow
  }

  .teste{
    background:  black;
  }
</style>