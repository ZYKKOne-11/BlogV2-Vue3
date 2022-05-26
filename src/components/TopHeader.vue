<script lang="ts" setup>
defineProps({
  size: Boolean,
})
</script>

<template>
  <header class="flex justify-between">
    <a v-if="!size" class="title" href="/">NoPatience</a>
    <a v-if="size" class="smallTitle" href="/">NoPatience</a>
    <DarkToggle />
  </header>
</template>

<style lang="scss" scoped>
.title {
  font-size: 2rem;
  font-weight: bolder;
}
.smallTitle {
  font-size: 1.5rem;
  font-weight: bolder;
  color: #FFA7C4;
}
</style>
