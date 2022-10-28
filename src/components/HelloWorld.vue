<script setup lang="ts">
import { computed } from "vue";
import type SimpleName from "./SimpleName.vue";


type Burrito = {
  __type__: "burrito";
};

type Salad = {
  __type__: "salad";
  dressing: string;
};

const props = defineProps<{
  food: Salad | Burrito;
}>();

const isSalad = computed(() => props.food.__type__ === "salad");
</script>

<template>
  <SimpleName :message="isSalad ? props.food.dressing : 'none'" />
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {

  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
