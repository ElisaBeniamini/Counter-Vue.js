<template>
    <h1>{{ state.counter }} </h1>
    <div class="container-button">
        <button @click="increment">Incrementa <br> +1</button>
        <button @click="decrement">Decrementa <br> -1</button>
        <button @click="reset">Reset</button>

    </div>

</template>


<script setup>
import { reactive } from "vue";
const state = reactive({
    counter: 0,
});
const increment = () => {
    state.counter++;
};
const decrement = () => {
    state.counter--;
};
const reset = () => {
    state.counter = 0;
};
</script>


<style>
button {
    color: rgb(255, 192, 203);
    background-color: rgba(0, 0, 0, 0.764);
}
</style>