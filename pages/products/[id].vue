<template>
  <div>
    <p>product details {{ id }}</p>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});
const { id } = useRoute().params;
</script>

<style lang="css" scoped></style>
