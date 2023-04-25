<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script>
export default {
  name: "About",
  methods: {
    load() {
      const shiki = require('shiki')

      shiki
          .getHighlighter({
            theme: 'nord'
          })
          .then(highlighter => {
            console.log(highlighter.codeToHtml(`console.log('shiki');`, { lang: 'js' }))
          })
    }
  },
  created() {
    this.load();
  }
}
</script>
