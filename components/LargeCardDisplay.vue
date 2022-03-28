<template>
  <div class="container">
    <h4 class="header">{{ largeCard.title }}</h4>
    <p class="snippet">
      {{ largeCard.snippet }}
    </p>
    <div class="cards-container">
      <LargeCard
        v-for="card in largeCard.cards"
        :key="card.image"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
import LargeCard from "./LargeCard.vue";
export default {
  props: ["largeCard"],
  components: { LargeCard },
};
</script>

<style scoped>
.container {
  margin-top: 2rem;
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
}
.snippet {
  color: grey;
  margin-bottom: 1.5rem;
}
.cards-container {
  display: flex;
  justify-content: space-between;
}
</style>
