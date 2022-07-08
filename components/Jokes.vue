<script>
import axios from 'axios'

export default {
    
    data() {
        return {
            jokes: []
        };
    },
    async created() {
        const config = {
            headers: {
                "Accept": "application/json"
            }
        };
        const result = await axios.get("https://icanhazdadjoke.com/search", config);
        this.jokes = result;
    },

   
}
</script>

<template>
    <div  class="flex flex-wrap justify-center" >
        <div v-for="(joke,index) in jokes.data?.results" :key="index" >
     
<nuxt-link :to="'dadJokes/' + joke.id">
    <span  class="flex flex-start gap-4 p-5 border mt-3 rounded-md w-40 h-40 mx-2 relative">
    
        <p class="truncate leading-2">
            {{joke.joke}}
        </p>
    
          <small class="absolute bottom-1 left-1 " >
            {{joke.id}}
        </small>
    </span>
</nuxt-link>
        </div>
       
    </div>
</template>