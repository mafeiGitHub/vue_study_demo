<script setup lang="ts">

import {ref} from "vue";

const text = ref("Edit me!");
const checked = ref(true);
const checkedNames = ref(['Jack']);
const picked = ref(true);
const selected = ref(true);
const multiSelected = ref(['A']);

</script>

<template>
    <h2>Text Input</h2>
    <input v-model="text">{{ text }}
    <h2>Check Box</h2>
    <input type="checkbox" id="checkbox" v-model="checked">{{ checked }}
    <h2>Multi Checkbox</h2>
    <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
    <label for="jack">jack</label>
    <input type="checkbox" id="tom" value="Tom" v-model="checkedNames">
    <label for="tom">tom</label>
    <input type="checkbox" id="jerry" value="Jerry" v-model="checkedNames">
    <label for="jerry">jerry</label>
    <p>checkedNames: {{ checkedNames }}</p>
  <!-- Radio-->
    <h2>Radio</h2>
    <input type="radio" id="one" value="One" v-model="picked">
    <label for="one">One</label>
    <input type="radio" id="two" value="Two" v-model="picked">
    <label for="two">Two</label>
    <br>
    <span>Picked: {{ picked }}</span>
    <h2>Select</h2>
    <select v-model="selected">
        <option disabled value="">Please select one</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>
    </select>
    <span>Selected: {{ selected }}</span>

    <h2>Multi Select</h2>
    <select v-model="multiSelected" multiple style="width: 100px;">
        <option>A</option>
        <option>B</option>
        <option>C</option>
    </select>
    <span>Selected: {{ multiSelected }}</span>
</template>

<style scoped>


</style>
