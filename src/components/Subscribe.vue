<script lang="ts" setup></script>

<template>
  <div class="sub-box">
    <div class="box-left"></div>
    <div class="box-right"></div>
  </div>
</template>

<style lang="scss" scoped>
.sub-box {
  display: flex;
  .box-left {
    flex-grow: 1;
  }
  .box-right {
    flex-grow: 1;
  }
}

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
