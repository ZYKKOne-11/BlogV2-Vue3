<script lang="ts" setup>
defineProps({
  text: String,
  href: String,
})
</script>

<template>
  <p>
    <a :href="href">
      {{ text }}
      <svg viewBox="0 0 70 36">
        <path
          d="M6.9739 30.8153H63.0244C65.5269 30.8152 75.5358 -3.68471 35.4998 2.81531C-16.1598 11.2025 0.894099 33.9766 26.9922 34.3153C104.062 35.3153 54.5169 -6.68469 23.489 9.31527"
        />
      </svg>
    </a>
  </p>
</template>

<style lang="scss" scoped>
:root {
  --text: #2b3044;
  --line: #bbc1e1;
  --line-active: #275efe;
}

p {
  font-size: 18px;
  margin-left: 5px;
  color: #d23669;
  a {
    display: inline-block;
    position: relative;
    text-decoration: none;
    color: inherit;
    margin: 0 var(--spacing, 0px);
    transition: margin 0.25s;
    svg {
      width: 76px;
      height: 40px;
      position: absolute;
      left: 50%;
      bottom: 0;
      transform: translate(-50%, 7px) translateZ(0);
      fill: none;
      stroke: var(--stroke, #bbc1e1);
      stroke-linecap: round;
      stroke-width: 2px;
      stroke-dasharray: var(--offset, 69px) 278px;
      stroke-dashoffset: 361px;
      transition: stroke 0.25s ease var(--stroke-delay, 0s),
        stroke-dasharray 0.35s;
    }
    &:hover {
      --spacing: 6px;
      --stroke: #d23669;
      --stroke-delay: 0.1s;
      --offset: 190px;
    }
  }
}
</style>
