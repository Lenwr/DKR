<script setup>

defineProps({
  category: String,
  description: String,
  name: String ,
  price: Number,
  picture: String
})
</script>

<template>
  <div class="p-2  ">
    <div class="flex  flex-row rounded-xl shadow-2xl opacity-1 bg-white ">
      <div class="w-1/3">
        <img class="w-full rounded-xl h-[7em]" src="https://img.freepik.com/photos-gratuite/cuisine-asiatique-dans-restaurant_7939-2024.jpg?t=st=1724746632~exp=1724750232~hmac=34e8eba5aff8279b2ed4e77b515692a771ee2be4d4883711571c258a7b56d8fa&w=1800" alt="">
      </div>
      <div class="w-2/3 flex flex-col justify-between p-2">
        <h1 class="font-semibold ">{{(name).toUpperCase()}}</h1>
        <p class="text-xs">{{description}}</p>
        <h1 class="font-semibold">{{price}} Euro</h1>
      </div>
    </div>
  </div>
</template>

<style scoped>


</style>
