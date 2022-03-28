<template>
  <NuxtLink :to="`/products/${card.id}`" class="card">
    <img
      class="image"
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt=""
    />
    <h3 class="header">{{ card.title }}</h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </NuxtLink>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
  color: #000;
}
.header:hover {
  color: #000;
  text-decoration: none;
}
.snippet {
  color: grey;
}
a {
  text-decoration: none;
  color: inherit;
}
</style>
