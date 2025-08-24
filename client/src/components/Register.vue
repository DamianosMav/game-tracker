<script setup>
import authenticationService from "../services/authenticationService"
import { ref } from "vue";


const email = ref("");
const password=ref("");

async function register(){
    const response = await authenticationService.register({
        email:email.value,
        password:password.value
    });

    console.log(response.data);
}

</script>

<template>
    <div>
        <h1>Register</h1>
        <input type="email" name="email" v-model="email" placeholder="email@test.com"></input>
        <br>
        <input type="password" name="password" v-model="password"></input>
        <br>
        <button @click="register">Submit</button>
    </div>
</template>

<stype>

</stype>