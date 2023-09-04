<script setup lang="ts">
import {ref} from "vue";
import TodoItem from "../components/TodoItem.vue";
const groceryList = ref([
    {id:0,text:'apple'},
    {id:1,text:'bpple'},
    {id:2,text:'cpple'},
    {id:3,text:'dpple'}
]);
</script>
<template>
<ol>
    <todo-item
    v-for="item in groceryList"
    :todo="item"
    :key="item.id"
    ></todo-item>
</ol>
</template>



<style scoped>

</style>