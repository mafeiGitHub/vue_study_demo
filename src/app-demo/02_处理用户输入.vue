<script setup lang="ts">
import {ref} from "vue";

const message = ref('hello world!')
function reverseMessage() {
    // message.value = message.value.split('').reverse().join('')
    message.value = message.value.split('').reverse().join('')
}
function notify() {
    alert('navigation was prevented.')
}
</script>

<template>
    <h1>{{ message }}</h1>
    <button @click="reverseMessage">reverseMessage</button>
    <div><button @click="message+='!'">append !</button></div>
    <div><a href="https://vuejs.org" >a herf </a></div>
    <a href="https://vuejs.org" @click.prevent="notify">a herf is been prevent!</a>
</template>

<style scoped>

</style>
