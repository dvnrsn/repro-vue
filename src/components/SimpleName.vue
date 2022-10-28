<script setup lang="ts">
const props = defineProps<{
  msg: string;
}>();
if (props.msg) {
  //awef
}
</script>

<template>
  <div class="greetings">props.msg</div>
</template>

<style scoped></style>
