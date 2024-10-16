<template>
  <div>
    <Header></Header>
    <div v-if="!x"><button @click="open">Click-open</button></div>
    <Main classOpen="classRegisterLogin" v-if="x"></Main>

    <Footer></Footer>
  </div>
  
  
</template>

<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Main from './components/Main.vue';
import { ref } from 'vue';

const x = ref(false);

const open =() => {
  x.value = !x.value;
}
</script>

<style>
button{
  margin: 10px 42% ;
  border-color: #2ca72c;
  color: #2ca72c;
}
</style>
