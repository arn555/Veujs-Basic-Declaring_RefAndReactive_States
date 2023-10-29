<script setup>

import {ref,reactive, isRef, isReactive} from 'vue';

// let count = ref(0);
// let name = ref("Krishna");

const num = reactive({count: 0})
const arr = reactive (["radhna", "ui", "ux"])
const num_arr = reactive({
    num: {count: 0},
    arr:["radhna", "gita", "seema"]
})

// console.log(num_arr);

const num_arr_with_ref = reactive({
    num: {count: ref(10)},
    arr:["radhna", "gita", "seema"]
})
 

setInterval(() =>{
    // console.log("value increased");
    // count.value++;
    // name.value = "radna";
    num.count++;
}, 1000 )

setTimeout(() => {
    arr.push("sita");
    num_arr.arr.push("dsdsf");
    num_arr.num.count++;
    num_arr_with_ref.num.count++;
}, 2000)

const a = ref(10);
const b = reactive({number: 10});

console.log(isRef(a)? "This is ref" : "this is not ref");
console.log(isReactive(b)? "This is reactive": "this is not reactive");


</script> 

<template>

    <h1> Hello World</h1>

    <h1> {{ num.count }}</h1>

    <h1>{{ arr }}</h1>

    <h1>{{ num_arr.arr }}</h1>
    <h1>{{ num_arr.num.count }}</h1>

    <h1>{{ num_arr_with_ref.num.count }}</h1>

</template>