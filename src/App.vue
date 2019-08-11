<template>
  <div id="app">
    <Product :product="product" :image="image" :inventory="inventory" :details="details"/>
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
      image: "../assets/logo.png",
      inventory: 1,
      details: ["80% cotton", "20% polyster", "Gender-neutral"]
    };
  }
};
</script>

<style>
</style>
