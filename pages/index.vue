<template>
  <div>
    <div class="grid grid-cols-3 gap-5">
      <div v-for="product in products">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>

<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products/");
</script>

<style lang="css" scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>
