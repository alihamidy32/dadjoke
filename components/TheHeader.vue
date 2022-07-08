<script>
export default {
    name:'TheHeader'
}
</script>

<template>
<div class=" bg-gray-100 border-box ">

    <header class="max-w-7xl mx-auto pt-4 flex justify-between items-center">
<ul class="flex flex-start gap-2 p-4 cursor-pointer">
    <li class="text-gray-600 py-1 px-4 border rounded-md">
        <nuxt-link to="/">Home</nuxt-link>

    </li>
      <li class="text-gray-600 py-1 px-4 border rounded-md">
          <nuxt-link to="/dadJokes">dadJoke</nuxt-link>

      </li>
    <li class="text-gray-600 py-1 px-4 border rounded-md">

        <nuxt-link to="/about">about</nuxt-link>
    </li>
</ul>

<h1 class="px-2 text-blue-200 text-xl">Dad Jokes!</h1>
  </header>
</div>
</template>

<style scoped>

li:hover{
    background-color: rgba(72, 70, 70, 0.864);
    color: rgba(222, 213, 213, 0.885);
}
</style>