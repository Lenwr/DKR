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
        <img class="w-full rounded-xl h-auto" src="https://img.freepik.com/photos-gratuite/cuisine-asiatique-dans-restaurant_7939-2024.jpg?t=st=1724746632~exp=1724750232~hmac=34e8eba5aff8279b2ed4e77b515692a771ee2be4d4883711571c258a7b56d8fa&w=1800" alt="">
      </div>
      <div class=" flex flex-col items-center justify-between p-2">
        <h1 class="font-semibold my-2 ">{{(name).toUpperCase()}}</h1>
        <p class="font-semibold my-2 text-center">{{type}}</p>
        <p class=" text-center">{{description}}</p>
        <h1 class="font-semibold my-2">{{price}} Euro</h1>
      </div>
    </div>
  </div>
</template>

<style scoped>


</style>
