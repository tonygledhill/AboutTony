<script setup lang="ts">
import Card from "./Card.vue";
import cards from "../data/cards.json";
import gsap from "gsap";

const afterEnter = () => {};

const beforeEnter = (el: any) => {
  el.style.opacity = 0;
  el.style.transform = "translateY(-60px)";
};

const enter = (el: any) => {
  gsap.to(el, {
    y: 0,
    opacity: 1,
    duration: 0.4,
    delay: el.dataset.index * 0.3,
  });
};
</script>

<template>
  <div class="cardblock">
    <div class="cardblock__container">
      <TransitionGroup
        name="card"
        appear
        @after-enter="afterEnter"
        @before-enter="beforeEnter"
        @enter="enter"
      >
        <Card
          v-for="(item, index) in cards.cards"
          :card="item"
          :key="index"
          :index="index"
          :data-index="index"
        >
        </Card>
      </TransitionGroup>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.cardblock {
  width: 100%;

  &__container {
    display: flex;
    gap: 1em;
  }
}
</style>
