<script setup lang="ts">
const props = defineProps<{
  msg: string;
}>();
</script>

<template>
  <div class="greetings">{{ props.msg }}</div>
</template>

<style scoped>

</style>
