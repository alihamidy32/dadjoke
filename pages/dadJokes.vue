<script>
import Jokes from '../components/Jokes.vue'
import TheHeader from '../components/TheHeader.vue'
export default {
    components:{TheHeader, Jokes}
}
</script>
<template>
    <div>
        <TheHeader/>
        <jokes/>
    </div>
    
</template>