/* eslint-disable */

<template>
    <div>
        <h2>Component E</h2>
        <ComponentF />
    </div>
</template>

<script>
import ComponentF from './ComponentF.vue';
    export default {
        name:'Component E',
        components:{
            ComponentF,
        }
    }
</script>

<style scoped>

</style>