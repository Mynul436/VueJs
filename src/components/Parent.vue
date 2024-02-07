<template>
<h2>I am From Parent Component</h2>
<ChildComponent name="Akash" :user="user" :getData="getData" />

<ChildComponent :getUser="getUserName" />

<h2 v-html="tag"></h2>
<h2 :class="applyStyle">
    I am From Parent Component for the class binding
</h2>

<button v-on:click="colorful = !colorful">Apply Style</button>
</template>

<script>
import ChildComponent from "./Child.vue";

export default {
    name: "ParentComponent",
    components: {
        ChildComponent,
    },
    data() {
        return {
            user: {
                name: "Kanon",
                age: 22,
            },
            tag: "<h4>I am from h4</h4>",
            colorful: true,
        };
    },
    methods: {
        getData() {
            console.warn("parent function is  called");
        },
        getUserName(name){
            alert(name)
        }
    },

    
    computed: {
        applyStyle() {
            return {
                green: this.colorful,
                err: true
            };
        }
    },

};
</script>

<style scoped>
h2 {
    color: cadetblue;
}

.green {
    background-color: greenyellow;
    width: 300px;
    padding: 10px;
}

.err {
    color: red;
}
</style>
