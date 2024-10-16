<template>
    <div v-if="!register">
        <div v-if="!login">
            <button :class="classOpen"  @click="openRegister">Register</button>
        </div>    
    </div>
    <div v-if="register"> 
        <Register/> 
    </div>


    <div v-if="!register" >
        <div v-if="!login">
            <button :class="classOpen" @click="openLogin">Login</button>
        </div>
    </div>
    <div v-if="login"> 
        <Login/> 
    </div>


</template>

<script setup>
import Register from './Register.vue';
import Login from './Login.vue';
import {ref} from 'vue';

const register = ref(false);
const login = ref(false);

const openRegister =() => {
    register.value = !register.value;
}
const openLogin =() => {
    login.value = !login.value;
}

const props = defineProps({
    classOpen: {
        type: String,
        required: true
    }
});
</script>

<style scoped>
</style>