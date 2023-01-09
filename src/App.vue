<template>
 <div>{{sum.name}}</div>
 <div>{{sum.age}}</div>
 <button @click="sum.name += '1'">+</button>
</template>

<script>

import { reactive, watch } from 'vue';

export default {
  name: 'App',
    setup() {

        let sum = reactive({
            name: 'wo',
            age: 20
        })
        watch(() => [sum.name, sum.age], (newValue, oldValue) => {
            console.log(newValue, oldValue);
        })
        return {
            sum
        }
    }
}
</script>

<style>

</style>
