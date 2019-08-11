<template>
  <div id="app">
    <Product
      :product="product"
      :image="image"
      :inventory="inventory"
      :details="details"
      :variants="variants"
      :cart="cart"
      :addtoCart="addtoCart"
    />
  </div>
</template>

<script>
import Product from "./components/Product";

export default {
  name: "App",
  components: {
    Product
  },

  methods: {
    addtoCart: function() {
      this.cart += 1;
    }
  },

  data() {
    return {
      product: "Socks",
      image: "../assets/logo.png",
      inventory: 1,
      details: ["80% cotton", "20% polyster", "Gender-neutral"],
      variants: [
        { variantId: 2344, variantColor: "blue" },
        { variantId: 2345, variantColor: "Green" }
      ],
      cart: 0
    };
  }
};
</script>

<style>
</style>
