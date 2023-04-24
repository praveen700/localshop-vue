<template>
    <div>
        Parent component
        <button @click="showChild = !showChild">Toggle Child</button>
        <Children v-if="showChild" />
    </div>
</template>

<script>
import Children from "./Child.vue"
    export default {
        components: { Children },
        name: 'ParentComponent',
        data(){
            return { 
                showChild: true,
            }
        },
        beforeCreate(){
            console.log("Parent before created")
        },
        created(){
            console.log("Parent created")
        },
        beforeMount(){
            console.log("Parent beforeMount")
        },
        mounted(){
            console.log("Parent mounted")
        },
        beforeUpdate(){
            console.log("Parent beforeUpdate")
        },
        updated(){
            console.log("Parent updated")
        },
        beforeUnmount(){
            console.log("Parent beforeUnmount")
        },
        unmounted(){
            console.log("Parent unmounted")
        }

    }
</script>

<style scoped>

</style>