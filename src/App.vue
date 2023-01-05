<template>
 <div>{{name}}</div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'App',
    setup() {
        let name = ref('wocao')
        console.log(name);
        return {
            name
        }
    }
}
</script>

<style>

</style>
