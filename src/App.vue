<template>
  <div id="app">
    <HeaderAlbums/>
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HeaderAlbums from './components/HeaderAlbums.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    HeaderAlbums
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}
</style>
