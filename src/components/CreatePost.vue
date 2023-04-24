<template>
    <div>
        <form @submit.prevent="createPosts">
            <div>
                <label for="userid">Post User iD</label>
                <input type="text" id="userId" v-model="formData.userId">
            </div>
            <div>
                <label for="title">Post  Title</label>
                <input type="text" id="title" v-model="formData.title">
            </div>
            <div>
                <label for="body">Post body</label>
                <input type="text" id="body" v-model="formData.body">
            </div>
            <button>Create Post</button>
        </form>
    </div>
</template>

<script>
import axios from 'axios';

    export default {
        name:'CreatePost',
        data(){
            return{
                formData: {
                    userId: '',
                    title:'',
                    body:'',

                }
            }
        },
        methods:{
            createPosts(){
                axios.post('https://jsonplaceholder.typicode.com/posts', this.formData)
                .then((res) => {
                   console.log(res)

                }).catch((err) => {
                    console.log(err)

                })

            }
        }
    }
</script>

<style scoped>

</style>