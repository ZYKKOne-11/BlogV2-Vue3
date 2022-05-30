<script lang="ts" setup>
const isInputVisible = ref(false)
const aboutData = ref({ name: '', words: '' })

const handleEditClick = () => {
  isInputVisible.value = !isInputVisible.value
}
const handleSendClick = () => {
  console.log(aboutData.value)
  aboutData.value.name = ''
  aboutData.value.words = ''
  isInputVisible.value = false
}
</script>
<template>
  <div class="wrapper">
    <div class="typing-demo">I don't Know.</div>
    <div class="title">说实话，我对自己一直感觉很迷。</div>
    <div v-if="!isInputVisible" class="edit" @click="handleEditClick">
      帮我客观的认清自己
      <icon-custom-pen />
    </div>
    <div v-if="isInputVisible" class="input-wrap">
      <input
        v-model="aboutData.name"
        type="text"
        class="input"
        placeholder="your name"
        style="margin-right: 20px"
      />
      <input
        v-model="aboutData.words"
        type="text"
        class="input"
        placeholder="your words"
      />
      <a class="send-btn" @click="handleSendClick">Send</a>
    </div>
    <div class="list">
      <div class="item-wrap">
        <span>我：</span>
        <span>我不一定是个好人，但是我一定是个善良的人</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  min-height: 80vh;
  padding-top: 20vh;
}
.title {
  margin-bottom: 40px;
}
.edit {
  font-family: 'Merriweather', 'Georgia', serif;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  cursor: pointer;
}
.input-wrap {
  font-family: 'Merriweather', 'Georgia', serif;
  .send-btn {
    margin-left: 10px;
    cursor: pointer;
  }
}
.input {
  border-bottom: 1px solid black;
  outline-style: none;
}

.list {
  font-family: 'Merriweather', 'Georgia', serif;
  margin-top: 5rem;
  .item-wrap {
    margin-bottom: 20px;
  }
}

.typing-demo {
  margin: 0 auto;
  width: 16ch;
  animation: typing 2s steps(16), blink 0.5s step-end infinite alternate;
  word-wrap: break-word;
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
  title: 我
</route>
