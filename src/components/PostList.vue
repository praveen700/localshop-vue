<template>
    <div>
        <input type="text" ref="inputRef" />
        <button @click="getPosts">Load Posts</button>
        <div v-for="post in posts" :key="post.id">
            <h3>{{ post.id }}, {{ post.title }}</h3>
            <p>{{ post.body }}</p>
            <hr />
        </div>
    </div>
</template>

<script>
import axios from 'axios';

    export default {
        name: 'PostList',
        data(){
            return {
                posts:[]
            }
        },
        created(){
            this.getPosts()
        },
        mounted(){
            this.$refs.inputRef.focus()
        },
        methods: {
            getPosts(){
                axios.get('https://jsonplaceholder.typicode.com/posts').then((res) => {
                    this.posts = res.data

                }).catch((err) => {
                    console.log(err)

                })

            }
        }
    }
</script>

<style scoped>

</style>