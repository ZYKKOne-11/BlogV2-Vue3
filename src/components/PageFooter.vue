<script lang="ts" setup>
defineProps({
  name: String,
})
</script>
<template>
  <footer class="bottom-0" w="full" text="center" p="y-2">
    <a class="link blue" href="/">NoPatience</a> · <a class="link green" href="#">KKO</a> ·
    <a class="link pink" target="_blank" href="https://github.com/ZYKKOne-11/">GitHub
    </a>
  </footer>
</template>

<style lang="scss" scoped>
.link {
   font-family: 'Merriweather', 'Georgia', serif;
    font-weight: 400;
    word-wrap: break-word;
    font-kerning: normal;
    -moz-font-feature-settings: "kern", "liga", "clig", "calt";
    -ms-font-feature-settings: "kern", "liga", "clig", "calt";
    -webkit-font-feature-settings: "kern", "liga", "clig", "calt";
    font-feature-settings: "kern", "liga", "clig", "calt";
}
.blue:hover {
  color: #70a1ff;
}

.pink:hover {
  color: #ff6b81;
}

.green:hover {
  color: #2ed573;
}
</style>
