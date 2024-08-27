<script setup>
import ArticleCard from "./components/articleCard.vue";
import {foodList} from "./constants.js";
import {computed, ref} from "vue";
import MenuCard from "./components/menuCard.vue";

const entréesItems = computed(() => {
  return foodList.filter(item => item.category === 'entrées');
});
const saladItems = computed(() => {
  return foodList.filter(item => item.category === 'salades');
});
const accompagnementsItems = computed(() => {
  return foodList.filter(item => item.category === 'accompagnements');
});
const menusItems = computed(() => {
  return foodList.filter(item => item.category === 'menu');
});
</script>

<template >
<div class="bg-yellow-400 p-2">
<h1 class="rounded-2xl p-4 bg-gray-300 bg-grey-300 font-semibold text-2xl text-center shadow-2xl" >DKR</h1>
  <div class="p-2">
    <img class="w-full rounded-2xl shadow-2xl" src="https://img.freepik.com/photos-gratuite/celebration-aid-al-fitr-cuisine-delicieuse_23-2151205125.jpg?t=st=1724744867~exp=1724748467~hmac=9fc590b4be77bc0ca00a15fd052f9e660d6b460e97a3be994687c8ef83479500&w=2000" alt="">
  </div>
  <div >
    <h1 class="px-2  text-2xl">Nos menus </h1>
    <ul v-for="item in menusItems" class=" " >
      <li class="md:w-[30%]"><menu-card :name=item.name :description=item.description :type=item.type :price=item.price :picture=item.picture /></li>
    </ul>
    <h1 class="px-2  text-2xl">Les entrées </h1>
    <ul v-for="item in entréesItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>
    <h1 class="px-2  text-2xl">Les Salades </h1>
    <ul v-for="item in saladItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>
    <h1 class="px-2  text-2xl">Les accompagements </h1>
    <ul v-for="item in accompagnementsItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

  </div>
</div>
</template>

<style scoped>
</style>
