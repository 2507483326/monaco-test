<template>
  <div id="app">
    <div ref='editor' class="editor_box"></div>
  </div>
</template>

<script>
// eslint-disable-next-line
import * as monaco from 'monaco-editor';
export default {
  mounted () {
    monaco.editor.create(this.$refs.editor, {
      value: [
        'function x() {',
        '\tconsole.log("Hello world!");',
        '}'
      ].join('\n'),
      language: 'javascript'
    })
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.editor_box{
  width: 500px;
  height: 500px;
}
</style>
