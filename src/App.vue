<script setup>
import ArticleCard from "./components/articleCard.vue";
import {foodList} from "./constants.js";
import {computed, ref} from "vue";
import MenuCard from "./components/menuCard.vue";
import VueHorizontal from 'vue-horizontal';

const entréesItems = computed(() => {
  return foodList.filter(item => item.category === 'entrées');
});
const supplyItems = computed(() => {
  return foodList.filter(item => item.category === 'supply');
});
const accompagnementsItems = computed(() => {
  return foodList.filter(item => item.category === 'accompagnements');
});
const menusItems = computed(() => {
  return foodList.filter(item => item.category === 'menu');
});
const drinkItems = computed(() => {
  return foodList.filter(item => item.category === 'boissons');
});
const dishesItems = computed(() => {
  return foodList.filter(item => item.category === 'plats');
});
const grillsItems = computed(() => {
  return foodList.filter(item => item.category === 'grillades');
});
const chickenItems = computed(() => {
  return foodList.filter(item => item.category === 'chicken');
});
const chickenMenuItems = computed(() => {
  return foodList.filter(item => item.category === 'menu');
});

const  items = [
  {
    title : 'ENTRÉE',
    id:'#entree'
  },
  {
    title : 'ACCOMPAGNEMENT',
    id:'#accommpagnements'
  },
  {
    title : 'SUPPLÉMENT',
    id:'#suppléments'
  },
  {
    title : 'NOS PLATS',
    id:'#plats'
  },
  {
    title : 'GRILLADES / DIBITERIE',
    id:'#grillades'
  },
  {
    title : 'BOISSONS',
    id:'#boissons'
  },
  {
    title : 'POULETS',
    id:'#poulets'
  },
  {
    title : 'NOS MENUS POULET',
    id:'#menu'
  },
]
</script>

<template >
<div class=" bg-[url('/background.jpg')]">
<div class="bg-white text-black ">
  <div class="p-2">
  <h1 class="rounded-2xl text-red-700 p-4 bg-yellow-500 bg-grey-300 font-semibold text-2xl text-center shadow-2xl" >DKR MENU</h1>
  </div>
  <div class="p-2">
    <img class="w-full rounded-2xl shadow-2xl" src="/logo.jpeg" alt="">
  </div>
  <div class="px-2">
    <vue-horizontal responsive>
      <section v-for="item in items" :key="item.title">
        <a :href=item.id >
          <div class="px-2 py-4 bg-white rounded shadow-2xl ">
            <h3>{{ item.title }}</h3>
            <p>{{ item.content }}</p>
          </div>
        </a>
      </section>
    </vue-horizontal>
  </div>
  <div >
    <h1 class="p-2 my-2 font-semibold text-2xl" id="entree">ENTRÉE </h1>
    <ul v-for="item in entréesItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

    <h1 class="p-2 my-2 font-semibold text-2xl" id="accompagnements">ACCOMPAGNEMENT </h1>
    <ul v-for="item in accompagnementsItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

    <h1 class="p-2 my-2 font-semibold text-2xl" id="suppléments">SUPPLÉMENT </h1>
    <ul v-for="item in supplyItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

    <h1 class="p-2 my-2 font-semibold text-2xl" id="plats">NOS PLATS </h1>
    <ul v-for="item in dishesItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

    <h1 class="p-2 my-2 font-semibold text-2xl" id="plats">GRILLADES / DIBITERIE </h1>
    <ul v-for="item in grillsItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

    <h1 class="p-2 my-2 font-semibold text-2xl" >DESSERTS 3€</h1>

    <h1 class="p-2 my-2 font-semibold text-2xl" id="boissons">BOISSONS </h1>
    <ul v-for="item in drinkItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

    <h1 class="p-2 my-2 font-semibold text-2xl" id="poulets">POULETS </h1>
    <ul v-for="item in chickenItems" class=" " >
      <li class="md:w-[30%]"><article-card :name=item.name :description=item.description :price=item.price :picture=item.picture /></li>
    </ul>

    <h1 class="p-2 my-2 font-semibold text-2xl" id="menu">NOS MENUS POULET </h1>
    <ul v-for="item in menusItems" class=" " >
      <li class="md:w-[30%]"><menu-card :name=item.name :description=item.description :type=item.type :price=item.price :picture=item.picture /></li>
    </ul>

  </div>
</div>
  <div class="toast">
    <div class="alert bg-yellow-500 border-0">
      <a href="#entree"><svg  xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6 text-black">
  <path stroke-linecap="round" stroke-linejoin="round" d="m15 11.25-3-3m0 0-3 3m3-3v7.5M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z" />
</svg>
</a>
    </div>
  </div>
</div>
</template>

<style scoped>
section {
  padding: 16px 8px;

}
</style>
