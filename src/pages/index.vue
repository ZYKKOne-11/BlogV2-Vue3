<script lang="ts" setup>
const router = useRouter()

function go(value: string) {
  if (value) router.push(`/hello/${encodeURIComponent(value)}`)
}
</script>
<template>
  <div class="wrap">
    <TopHeader />
    <InfoLable />
    <!-- <div class="my-4">Index View <IconCustomFace /></div> -->
    <main>
      <article>
        <header>
          <h3 @click="go('测试标题嘎嘎长的标题！！！！！！！')">测试标题嘎嘎长的标题！！！！！！！</h3>
          <small>星期五，21日，7月，2021 · ❤️</small>
        </header>
        <p>
          让我把代码变的整洁吧！～让我把代码变的整洁吧！～让我把代码变的整洁吧！～让我把代码变的整洁吧！～让我把代码变的整洁吧！～
        </p>
      </article>
      <article>
        <header><h3>测试标题嘎嘎长的标题！</h3></header>
        <small>星期五，21日，7月，2021 · ❤️</small>
        <p>让我把代码变的整洁吧！～</p>
      </article>
      <article>
        <header><h3>测试标题嘎嘎长的标题！！！</h3></header>
        <small>星期五，21日，7月，2021 · ❤️</small>
        <p>让我把代码变的整洁吧！～</p>
      </article>
    </main>
    <BasicHello />
  </div>
</template>

<style lang="scss" scoped>
.wrap {
  max-width: 42rem;
  margin-left: auto;
  margin-right: auto;
  main {
    margin-top: 5rem;
    article {
      margin-bottom: 4rem;
      text-align: left;
      header {
        margin-bottom: 0.2rem;
        h3 {
          color: #d23669;
          font-size: 1.75rem;
          font-weight: bolder;
          letter-spacing: 0.1rem;
          text-rendering: optimizeLegibility;
          font-size: 1.4427rem;
          line-height: 1.1;
          cursor: pointer;
          margin-bottom: 1rem;
        }
        small {
          font-family: 'Merriweather', 'Georgia', serif;
          font-weight: 400;
          word-wrap: break-word;
          font-kerning: normal;
          -moz-font-feature-settings: 'kern', 'liga', 'clig', 'calt';
          -ms-font-feature-settings: 'kern', 'liga', 'clig', 'calt';
          -webkit-font-feature-settings: 'kern', 'liga', 'clig', 'calt';
          font-feature-settings: 'kern', 'liga', 'clig', 'calt';
        }
      }
      p {
        font-family: 'Merriweather', 'Georgia', serif;
        font-weight: 400;
        word-wrap: break-word;
        font-kerning: normal;
        -moz-font-feature-settings: 'kern', 'liga', 'clig', 'calt';
        -ms-font-feature-settings: 'kern', 'liga', 'clig', 'calt';
        -webkit-font-feature-settings: 'kern', 'liga', 'clig', 'calt';
        font-feature-settings: 'kern', 'liga', 'clig', 'calt';
      }
    }
  }
}
</style>
