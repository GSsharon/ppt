<!--
 * @Author: sharon
 * @Date: 2020-12-29 16:47:27
 * @LastEditTime: 2020-12-29 19:52:08
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \ppt\src\components\Container.vue
-->
<template>
  <div class="pptContainer">
    <Page v-for="(page,idx) in options" :key="idx" :pageTitle="page.title" :content="page.content"></Page>
  </div>
</template>
<script>
import Page from "./Page"
export default {
  name: 'Container',
  components: {
    Page
  },
  props: {
    options: {
      type: Array,
      default() {
        return [];
      }
    }
  },
  created() {
    console.log(this.options)
  },
  data() {
    return {
    }
  }
}
</script>