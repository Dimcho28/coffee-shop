<template>
    <div class=" container mx-auto mt-20 ">
        <h1 class="text-3xl font-bold text-[#BC9667] text-center">OUR POPULAR PRODUCTS</h1>

        <div class="space-y-10 mt-10 max-lg:flex">
            <div class="grid grid-cols-3 max-w-6xl gap-y-10 mx-auto max-lg:grid-cols-1">
                <div v-for="coffee in coffees">
                    <ProductCard :image="coffee.img" :title="coffee.title" :price="coffee.price"/>
                </div>
            </div>
        </div>

    </div>
</template>

<script setup>
import ProductCard from './ProductCard.vue'
const coffees = [
  {
    title: "Espresso",
    price: 2.99,
    img: "/card.png"
  },
  {
    title: "Latte",
    price: 3.99,
    img: "/card2.png"
  },
  {
    title: "Cappuccino",
    price: 3.49,
    img: "/card3.png"
  },
  {
    title: "Americano",
    price: 2.49,
    img: "/card4.png"
  },
  {
    title: "Mocha",
    price: 4.49,
    img: "/card5.png"
  },
  {
    title: "Macchiato",
    price: 3.99,
    img: "/card6.png"
  },
];
</script>