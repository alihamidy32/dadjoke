<!-- Please remove this file from your project -->
<template>

<div>
    <TheHeader />
    <div class="flex flex-wrap justify-center">
        
        <Users v-for="(user,index) in users" :key="index" class="flex flex-wrap m-5" :users="user"/>
    </div>
</div>
</template>

<script>
import Users from './Users.vue'
import axios from 'axios'
import TheHeader from './TheHeader.vue'


    export default {
        components: {
            TheHeader,
                Users
        },
            data(){
        return{
            users:[]
        }
    },
    async created(){
        const result = await axios.get('https://jsonplaceholder.typicode.com/comments')
        this.users = result.data
    }
    }
</script>
