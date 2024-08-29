<script setup>

defineProps({
  category: String,
  description: String,
  name: String ,
  type:String,
  price: Number,
  picture: String
})
</script>

<template>
  <div class="p-2  ">
    <div class="flex  flex-col rounded-xl  opacity-1 bg-white ">
      <div class="">
        <img class="w-full rounded-xl h-auto" :src="picture" alt="">
      </div>
      <div class=" flex flex-col items-center justify-between p-2">
        <h1 class="font-semibold my-2 ">{{(name).toUpperCase()}}</h1>
        <p class="font-semibold my-2 text-center">{{type}}</p>
        <p class=" text-center">{{description}}</p>
        <h1 class="font-semibold my-2">{{price}} €</h1>
      </div>
    </div>
  </div>
</template>

<style scoped>


</style>
