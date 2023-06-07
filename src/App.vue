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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
