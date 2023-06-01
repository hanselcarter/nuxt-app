<template>
  <div>
    <h2>About</h2>
    <p>
      {{ value }}
      <br />
      Thank You!
    </p>
  </div>
</template>

<script setup>
const {
  data: { value },
} = await useFetch("/api/description");
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
