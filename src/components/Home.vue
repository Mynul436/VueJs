<template>
<h1>Home Component</h1>
<h1>Email : {{ email }}</h1>
<h2>Mobile : {{ mobile }}</h2>
<h2>Name : {{ getName() }}</h2>
<h2>FullName : {{ fullName() }}</h2>
<h2>Age : {{ age(24) }}</h2>
<button v-on:click="test()">Click Me</button>
<button v-on:click="test1()">Click Me for count</button>
<h2>{{ count }}</h2>
<input type="text" v-model="abc" />
<h2>{{ abc }}</h2>
<input type="text" placeholder="email" v-model="email2">
<br><br>
<input type="text" placeholder="password" v-model="password">
<br> <br>
<button v-on:click="buttonFunction()">Submit </button>
</template>

<script>
export default {
    name: "Home", // eslint-disable-line vue/multi-word-component-names

    data() {
        return {
            email: "mynul@gmail.com",
            mobile: 1234567,
            email2: null,
            password: null,
            getName: function () {
                return "mynul islam " + " " + this.email;
            },

            //   buttonFunction:function(){
            //     console.warn("value : "+this.email2,this.password)
            //   },

            count: 0,
            abc: 6,
        };
    },
    methods: {
        fullName() {
            return "Mynul Islam " + this.email;
        },
        age(a) {
            return a;
        },
        test() {
            // console.log("sfasaf")
            alert("function is clicked ");
        },
        test1() {
            // console.log("sfasaf")
            this.count = this.count + 1;
            console.log(this.count);
        },
        buttonFunction() {
            console.warn("value : " + this.email2, this.password)
        }
    },
};
</script>

<style scoped>
h1 {
    color: rgb(212, 196, 255);
}
</style>
