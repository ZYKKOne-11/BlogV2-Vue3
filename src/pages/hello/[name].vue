<script lang="ts" setup>
import { marked } from 'marked'
import './github-markdown.css'

const props = defineProps({ name: String })

const route = useRoute()
const data = JSON.parse(route?.query?.article as string)

const compileHtml = shallowRef()

compileHtml.value = marked(data.content, {
  renderer: new marked.Renderer(),
  // eslint-disable-next-line object-shorthand

  langPrefix: 'hljs language-',
  breaks: false,
  gfm: true,
  headerIds: true,
  headerPrefix: '',
  mangle: true,
  pedantic: false,
  sanitize: false,
  silent: false,
  smartLists: false,
  smartypants: false,
  xhtml: false,
})
</script>
<template>
  <div class="wrap">
    <TopHeader size="small" />
    <div class="my-5 mt-20">
      <div class="mb-5 font-bold">
        <span class="text-3xl title">{{ data.title }}</span>
        <div class="markdown-body" v-html="compileHtml"></div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrap {
  max-width: 42rem;
  margin-left: auto;
  margin-right: auto;
  text-align: left;
}
.markdown-body {
  box-sizing: border-box;
  min-width: 200px;
  max-width: 980px;
  margin: 0 auto;
  padding-top: 40px;
  background: 0 0;
  font: 100%/1.75 'Merriweather','Georgia',serif;
}
@media (max-width: 767px) {
  .markdown-body {
    padding: 5px;
  }
}
</style>
