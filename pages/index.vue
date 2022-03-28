<template>
  <div class="container">
    <Hero />
    <LargeCardDisplay
      v-for="largeCard in largeCards"
      :key="largeCard.id"
      :largeCard="largeCard"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCards"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "../assets/data";
import Hero from "../components/Hero.vue";
import LargeCardDisplay from "../components/LargeCardDisplay.vue";
import SmallCardDisplay from "../components/SmallCardDisplay.vue";
import Nav from "../components/Nav.vue";
export default {
  name: "IndexPage",
  data() {
    return {
      largeCards: largeCardSections,
      smallCards: smallCardSections,
    };
  },

  components: { Hero, LargeCardDisplay, SmallCardDisplay, Nav },
};
</script>
