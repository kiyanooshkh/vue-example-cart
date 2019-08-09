<template>
  <div class="product">
    <div class="product-image">
      <img :src="image">
    </div>
    <div class="product-info">
      <h1>{{product}}</h1>
      <p v-if="inventory > 10">In stock</p>
      <p v-else-if="inventory <= 1 && inventory > 0">Almost sold out</p>
      <p v-else>Out of stock</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Product",
  props: {
    product: String,
    image: String,
    inventory: Number
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.product-image img {
  width: 200px;
  height: 200px;
  background-color: red;
}
</style>