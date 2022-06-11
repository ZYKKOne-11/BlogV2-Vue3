<script lang="ts" setup>
type article = {
  cid: number
  content: string
  title: string
  description: string
  created: string
  date: string
}

const router = useRouter()
const articleList = ref<article[]>([])
const getList = async () => {
  fetch('/core-api/blog/article', {
    method: 'GET',
  })
    .then(res => res.json())
    .then(data => {
      articleList.value = data.data
    })
}

getList()

function go(value: any) {
  if (value) {
    router.push({
      path: `/hello/${encodeURIComponent(value.id)}`,
    })
  }
}
</script>
<template>
  <div class="wrap">
    <TopHeader />
    <InfoLable />
    <!-- <div class="my-4">Index View <IconCustomFace /></div> -->
    <main>
      <article v-for="item in articleList" :key="item.cid">
        <header>
          <h3 @click="go(item)">{{ item.title }}</h3>
          <small>{{ item.date }}</small>
        </header>
        <p>
          {{ item.description }}
        </p>
      </article>
    </main>
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
