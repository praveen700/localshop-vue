<template>
    <div>
        <h2>Welcome to Article {{ title }}</h2>
        <h2>Likes {{ Likes }}</h2>
        <h2>isPublished {{ isPublished ? 'Yes' : 'No' }}</h2>
    </div>
</template>

<script>
    export default {
        name:'Article',
        props: {
            title:{
                type: String,
                required: true,
            },
            Likes: Number,
            isPublished: Boolean,
        }
    }
</script>

<style scoped>

</style>