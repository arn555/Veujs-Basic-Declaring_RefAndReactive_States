<script setup>

let count = 0;

setTimeout(() =>{
    console.log("value increased");
    count++;
    console.log("value increased ", count);
}, 2000 )

</script> 

<template>

    <h1> Hello World</h1>

    <h1> {{ count }}</h1>

</template>