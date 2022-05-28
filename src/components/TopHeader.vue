<script lang="ts" setup>
defineProps({
  size: String,
})
</script>

<template>
  <header class="flex justify-between">
    <a
      :class="size === 'small' ? 'smallTitle' : 'title'"
      href="/"
    >
      NoPatience
    </a>
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
  color: #ffa7c4;
}
</style>
