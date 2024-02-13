<script setup>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
import HelloWorldComponent from './HelloWorldComponent.vue'
import {reactive} from 'vue'
import { ref } from 'vue';
const name="Hello world"
const isDisabled=false
const myData='jack'
function disp(){
    console.warn("Heloorsafas")
}
const objectatr={
    id:"jack",
    herf:"https://www.google.com/"
}

// let num=reactive({a:20,b:30})
// let num={a:20,b:30}

// num.a=80


const obj=reactive({
    num:{count:0},
    user:["Rhul","Soad"]
});
let numRef1= ref(10);

let numRef2= ref(30);
setTimeout(()=>{
console.log("Set time out calssed ");
// console.log("OBJ",obj)
// console.log("OBJ",obj.user)
// console.log("OBJ",obj.num)
// console.log("OBJ",obj.num.count)
// obj.num.count++
// obj.user.push("Mynul")
console.log("a : ",numRef1);
console.log("a : ",numRef2);
console.log("a.value : ",numRef1.value);
console.log("b.value : ",numRef2.value);
numRef1.value=70
console.log("after : ",numRef1.value)

},2000)

import {  computed } from 'vue'

const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
})

// a computed ref
const publishedBooksMessage = computed(() => {
  return author.books.length > 0 ? 'Yes' : 'No'
})


</script>

<template>
<!-- 
<h1>Count : {{ obj.num.count }}</h1>


<h1>User name : {{ obj.user }}</h1>

<h1>Sum : {{numRef1+numRef2  }}</h1> -->

<p>Has published books:</p>
  <span>{{ publishedBooksMessage }}</span>






  <!-- <h1>	Local Registration from {{ name }}</h1>
  {{ disp() }}

  <h3 v-bind:id="myData">MyData </h3>
<br>
  <button disabled>Vsit</button>
  <br>
  <br>
<button :disabled="isDisabled"> Visit2</button>
<br>
<h1>Sum {{ num.a+num.b }}</h1> -->


</template>

<style scoped>

</style>
