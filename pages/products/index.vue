<template>
  <div class="container">
    <LargeCardDisplay
      v-for="largeCard in largeCardSections.slice(0, 1)"
      :key="largeCard.id"
      :largeCard="largeCard"
    />
    <SmallCardDisplay
      v-for="cardsSection in smallCardSections"
      :key="cardsSection.id"
      :cardsSection="cardsSection"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "../../assets/data";
import LargeCardDisplay from "../../components/LargeCardDisplay.vue";
import SmallCardDisplay from "../../components/SmallCardDisplay.vue";
import Nav from "../../components/Nav.vue";
export default {
  data() {
    return {
      largeCardSections: largeCardSections,
      smallCardSections: smallCardSections,
    };
  },

  components: { LargeCardDisplay, SmallCardDisplay, Nav },
};
</script>

<style scoped></style>
