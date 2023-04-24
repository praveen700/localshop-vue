<template>
    <h3 v-for="name in names" :key="name.firstName">
        <slot :firstName="name.firstName"></slot>
        <slot :lastName="name.lastName"></slot>

    </h3>
</template>

<script>
    export default {
        name:'NameList',
        data(){
            return{
                names: [
                    {
                        firstName: "Praveen",
                        lastName: "MR"
                    },
                    {
                        firstName: "Naveen",
                        lastName: "MR"
                    },
                    {
                        firstName: "Ashok",
                        lastName: "MR"
                    }
                ]
            }
        }
    }
</script>

<style scoped>

</style>