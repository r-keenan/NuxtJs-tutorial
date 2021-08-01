<template>
  <div>
    <h1>This is the products page</h1>
    <input type="text" v-model="productId" />
    <button @click="onLoadProduct">Load Product</button>
    <div>
      <h3>Check out our most popular products</h3>
      <nuxt-link to="/products/1">Product 1</nuxt-link>
      <nuxt-link to="/products/2">Product 2</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      productId: ""
    };
  },
  methods: {
    onLoadProduct() {
      this.$router.push("/products/" + this.productId);
    }
  }
};
</script>
