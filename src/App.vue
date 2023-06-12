<template>
  <div id="app">
    <PageComponent/>
  </div>
</template>


<script>
import PageComponent from './PageComponent.vue'

export default {
  name: 'App',
  components: {
    PageComponent,
  }
}
</script>

<style>
body {
  background-color: #EFF3FF;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}
</style>
