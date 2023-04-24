/* eslint-disable */

<template>
    <div>
        <h2>Component F username {{ username }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'Component F',
        inject: ['username']
    }
</script>

<style scoped>

</style>