<script>

export default {
    props:['users'],


}
</script>

<template>
<div  class="bg-slate-600 max-w-lg flex flex-col justify-start rounded-tr-3xl rounded-bl-3xl rounded-tl-md rounded-br-md p-5">

    <div class="flex gap-2 ">
        <div class="w-20 h-20 bg-sky-100 border rounded-full border-gray-300 relative">
            <p class="absolute -translate-x-2/4 -translate-y-2/4 top-2/4 left-2/4 text-3xl text-zinc-500">{{(users.name).slice(0,2)}}</p>
        </div>

        <div class="flex flex-col">
             <p class="text-xs text-slate-50 my-3">{{'name :' + users.name}}</p>
             <p class="text-xs text-slate-50 ">{{'e-mail :' + users.email}}</p>
         </div>
    </div>
    <div class="mt-5">
        <h3 class="text-slate-300">
            {{users.body}}
        </h3>
    </div>
</div>
</template>