<template>
  <aside class="my-4 flex">
    <div class="w-14 rounded-full">
      <img class="w-14 rounded-full" src="@/assets/avaimg.png" alt="" />
    </div>
    <div class="info">
      <span>Personal blog by <span style="color: #ff6b81"> ZYKKOne.</span></span>
      <span>" a Funny Coder "（ 也许是个艺术家或肥宅,</span>
    </div>
  </aside>
</template>

<style lang="scss" scoped>
.info {
  text-align: left;
  margin-left: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  span {
    font-family: 'Merriweather', 'Georgia', serif;
    font-weight: 400;
    word-wrap: break-word;
    font-kerning: normal;
    -moz-font-feature-settings: "kern", "liga", "clig", "calt";
    -ms-font-feature-settings: "kern", "liga", "clig", "calt";
    -webkit-font-feature-settings: "kern", "liga", "clig", "calt";
    font-feature-settings: "kern", "liga", "clig", "calt";
  }
}
</style>
