<template>
  <div id="app">
    <Content/>
    <SideBar/>
    <Popup/>
  </div>
</template>

<script>
import Content from './components/Content.vue'
import SideBar from './components/SideBar.vue'
import Popup from './components/Popup.vue'

export default {
  name: 'App',
  components: {
    Content,
    SideBar,
    Popup
  }
}
</script>

<style>
#app {
  font-family: Lato, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #101010;
  margin-top: 60px;
}
</style>
