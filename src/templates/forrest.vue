<template>
  <base-layout :nav="$page.content.nav">
  <div @click="testQueryContent()">CLICK ME</div>
    <VueRemarkContent class="content" />
  </base-layout>
</template>

<script>
import BaseLayout from "../layouts/BaseLayout";

export default {
  name: "Content",
  components: { BaseLayout },
  methods: {
    testQueryContent() {
      console.log({
        title: this.$page.content.title,
        content: this.$page.content.title,
        nav: this.$page.content.title
      })
    }
  }
};
</script>

<page-query>
query ($id: ID!) {
  content(id: $id) {
    title
    content
    nav
  }
}
</page-query>

<style lang="scss">
.content {
  padding-bottom: $gutter-xlarge;
}
</style>
