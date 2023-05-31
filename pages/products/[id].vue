<template>
  <div>
    <p>{{ product.title }}</p>
    <p>{{ product.description }}</p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const uri = `https://fakestoreapi.com/products/${id}`;

const { data: product } = await useFetch(uri, { key: id });

definePageMeta({
  layout: "products",
});
</script>

<style lang="css" scoped></style>
