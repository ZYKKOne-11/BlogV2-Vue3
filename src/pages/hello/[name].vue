<script lang="ts" setup>
const props = defineProps({ name: String })
</script>
<template>
  <div class="wrap">
    <TopHeader size="small" />
    <div class="my-5">
      <div class="mb-5 font-bold">
        <span class="text-3xl ml-2">{{ props.name }}</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrap {
  max-width: 42rem;
  margin-left: auto;
  margin-right: auto;
}
</style>
