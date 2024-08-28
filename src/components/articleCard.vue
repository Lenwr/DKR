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
    <div class="flex bg-gray-100  flex-row rounded shadow opacity-1 bg-white ">
      <div class="w-1/3">
        <img class="w-full object-fit rounded h-[6em]" :src=picture alt="">
      </div>
      <div class="w-2/3 flex flex-col justify-around p-2">
        <h1 class="font-semibold text-[1.2em]">{{(name).toUpperCase()}}</h1>
        <p class="text-xs">{{description}}</p>
        <h1 class="text-[1.2em]">{{price}} Euro</h1>
      </div>
    </div>
  </div>
</template>

<style scoped>


</style>
