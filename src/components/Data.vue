/* eslint-disable */ 
<template>
    <h2>
        Options- {{ o_firstName }}
    </h2>
    <h2>Composition - {{ c_firstName }}</h2>
    <h2>Composition - {{ geetHero }}</h2>
    <h2>Composition - {{ reactGreet }}</h2>
    
</template>

<script>
import { ref, reactive } from "vue";

    export default {
        name:'Data',
        setup(){
            const c_firstName = ref('Clark');
            const c_lastName = ref('John')
            const geetHero = `Hello ${c_firstName.value} ${c_lastName.value}`
            const state = reactive({
               firstName : "Praveen",
               lastName: "MR",
               heroName: "Wonder Karnataka"
            })
            const reactGreet = `Hello ${state.firstName} ${state.lastName} ${state.heroName}`
            return { c_firstName, geetHero, reactGreet}

        },
        data(){
            return {
                o_firstName: 'Praveen'
            }
        }
    }
</script>

<style scoped>

</style>