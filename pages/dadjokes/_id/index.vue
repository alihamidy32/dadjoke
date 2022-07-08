<script>
import axios from 'axios'
import TheHeader from '../../../components/TheHeader.vue'
export default {
    components:{TheHeader},
    data(){
        return{
            joke:{}
        }
    },
    async created(){
        const config={
            headers:{
                
                "Accept":"application/json"
            }
        }
const result = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`,config)
this.joke = result
    },
    head(){
        return{
            title:this.joke.data?.joke,
            meta:[
                {
                    hid:'description',
                    name:'description',
                    content:'Best Place for corny jokes...'
                }
            ]
        }
    }
}
</script>
<template>
<div>
  <TheHeader/>
  <div class="bg-gray-50  my-5">
    <nuxt-link to="/dadJokes" class="mx-5 border rounded-lg px-4 py-2 text-gray-600">
        Back to Jokes
    </nuxt-link>
    <h3 class="mx-5 my-5 text-2xl">
        {{joke.data?.joke + ' :)))'}}
    </h3>
    <hr>
    <small class="mx-5">
        {{joke.data?.id}}
    </small>
  </div>
</div>
</template>