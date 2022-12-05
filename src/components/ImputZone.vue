<script setup>
import { ref } from 'vue';
import {computed} from 'vue';
        let text = ref('');
        /* text.value = "" */
        let save = ref('');
    //MEHTODS
        function SaveText(param){
            save.value=param;
        }
</script>
<template>
    <input type="text" name="" id="user" v-model="text">
    <h1>{{save}}</h1>
    <button @click="SaveText(text)">add</button>
</template>
<style lang="scss">
</style>