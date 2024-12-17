<script setup>

defineProps({
  category: String,
  description: String,
  name: String ,
  price: Number,
  picture: String,
})
</script>

<template>
  <div class="p-2 m-1.5 h-[14em] md:h-auto opacity-1 bg-white rounded-2xl   ">
    <div class="flex flex-col">
      <div class="">
        <img class="w-full object-cover h-[9em] md:h-[14em] rounded " :src=picture alt="">
      </div>
        <div class=" flex flex-col  justify-between p-2">
          <h1 class="font-semibold text-[#4c0c0d] text-xs ">{{(name).toUpperCase()}}</h1>
          <p class="text-xs text-[#4c0c0d]">{{description}}</p>

          <div class="flex flex-row justify-between">
            <h1 class="text-[#f88b32] text-lg">€ {{price}} </h1>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6 bg-green-500 rounded-full text-white p-1">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 20.25c4.97 0 9-3.694 9-8.25s-4.03-8.25-9-8.25S3 7.444 3 12c0 2.104.859 4.023 2.273 5.48.432.447.74 1.04.586 1.641a4.483 4.483 0 0 1-.923 1.785A5.969 5.969 0 0 0 6 21c1.282 0 2.47-.402 3.445-1.087.81.22 1.668.337 2.555.337Z" />
            </svg>
          </div>

      </div>

    </div>
  </div>
</template>

<style scoped>


</style>
