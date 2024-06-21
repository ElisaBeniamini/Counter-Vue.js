<template> 
<h1>{{ state.counter }}</h1>

<button @click="increment">Incrementa</button> 
<button @click="decrement">Decrementa</button>
<button @click="reset">Reset</button>
</template>


<script setup>
import { reactive } from "vue";
const state=reactive({
    counter:0,
});
const increment =()=>{
    state.counter++;
};
const decrement =()=>{
    state.counter--;
};
const reset =()=>{
    state.counter=0;
};
</script>


<style>
button{
    color:pink;
    background-color:black;
}
</style>