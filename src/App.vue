<template>
  <div id="app">
    <Product :product="product" :image="image" :inventory="inventory"/>
  </div>
</template>

<script>
import Product from "./components/Product";

export default {
  name: "App",
  components: {
    Product
  },

  data() {
    return {
      product: "Socks",
      image: "./assets/vmSock-green.jpg",
      inventory: 1
    };
  }
};
</script>

<style>
</style>
