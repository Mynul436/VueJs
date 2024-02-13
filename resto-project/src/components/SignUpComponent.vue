<template>
<img class="logo" src="../assets/restaurant9491.logowik.com.webp" width="150px" alt="">
<h1>Sign Up</h1>
{{ name }}
<div class="register">
    <input type="text" placeholder="Enter Name : " v-model="name">
    <input type="text" placeholder="Enter Email : " v-model="email">
    <input type="text" placeholder="Enter Password : " v-model="password">
    <br>
    <button v-on:click="signUp"> Sign Up </button>

</div>
</template>

<script>

import axios from 'axios'
export default {
    name: 'SignUpComponent',
    data() {
        return {
            name: '',
            email: '', 
            password: ''
        }
    },
    methods:{
      async  signUp(){
            console.warn("Sign Up",this.name,this.email,this.password)

            let result =await axios.post("http://localhost:3000/user",{name:this.name,email:this.email,password:this.password});

            console.warn(result)
            if(result.status==201){
                alert("sign up done")
            }
            localStorage.setItem("user-info",JSON.stringify(result.data))
        }

    }
}
</script>

<style>


.register input {

    width: 300px;
    height: 40px;
    padding-left: 20px;
    display: block;
    margin-bottom: 30px;
    margin-left: auto;
    margin-right: auto;
    border: 1px solid skyblue;

}

.register button {

    width: 320px;
    height: 40px;
    border: 1px solid skyblue;
    color: white;
    background-color: skyblue;

    cursor: pointer;
}
</style>
