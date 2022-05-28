<template>
  <div class="wrapper">
    <div class="typing-demo">There is nothing.</div>
    <div class="title">你在这里想找到什么呢？宝贝</div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  margin-top: 30vh;
  display: grid;
  place-items: center;
}

.typing-demo {
  width: 22ch;
  animation: typing 2s steps(22), blink 0.5s step-end infinite alternate;
  white-space: nowrap;
  overflow: hidden;
  border-right: 3px solid;
  font-family: monospace;
  font-size: 2em;
}

@keyframes typing {
  from {
    width: 0;
  }
}

@keyframes blink {
  50% {
    border-color: transparent;
  }
}
</style>

<route lang="yaml">
meta:
  layout: 404
</route>
