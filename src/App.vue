<script setup>
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';
import About from './components/About.vue';
import Products from './components/Products.vue';
import Customers from './components/Customers.vue';
</script>

<template>
  <Navbar />
  <Home />
  <About id="about"/>
  <Products id="products"/>
  <Customers />
</template>