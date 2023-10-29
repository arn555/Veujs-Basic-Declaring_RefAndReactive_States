<script setup>

import {ref} from 'vue';

let count = ref(0);
let name = ref("Krishna");

setTimeout(() =>{
    console.log("value increased");
    count.value++;
    name.value = "radna";
    console.log("value increased ", count);
}, 2000 )

</script> 

<template>

    <h1> Hello World</h1>

    <h1> {{ count }}</h1>
    <h1> {{ name }}</h1>

</template>