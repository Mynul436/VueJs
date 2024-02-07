<template>
<!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
<HelloWorld msg="Welcome To LL" />
<!-- <Home/> -->
<CheckBox />
<!-- <ChildComponent/> -->
<ParentComponent />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
// import Home from "./components/Home.vue";
import CheckBox from "./components/CheckBox.vue";
import ParentComponent from "./components/Parent.vue";

export default {
    name: "App",
    components: {
        HelloWorld,
        // Home,
        CheckBox,
        // ChildComponent,
        ParentComponent
    },
};
</script>

<!-- 
<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style> -->
