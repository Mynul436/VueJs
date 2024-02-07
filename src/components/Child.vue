<template>
<h2>I am From Child Component </h2>
<h2>{{ name }}</h2>
<h2>{{ user.age }}</h2>
<button v-on:click="getData(userName)">Click Me </button>
<br><br>

<button v-on:click="getUser">Get User Name </button>

</template>

<script>
export default {
    name: 'ChildComponent',
    props: {
        name: String,
        user: Object,
        getData: Function,
        getUser:Function,
    },

    data(){
        return {
            userName:"Peter"
        }
    },

   


}
</script>

<style scoped>
h2 {
    color: chocolate;
}
</style>
