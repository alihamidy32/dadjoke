<template>
  <Home/>
</template>

<script>
export default {
  name: 'IndexPage', 
  head(){
    return{
      title:'Dad Jokes',
      meta:[
        {
          hid:  'description',
          content:'Best place for corny dad jokes...',
          name:'description'
        }
      ]
    }
  }
}
</script>
