<template>
  <div class="app">
    <MainComponent />
  </div>
</template>

<script>
import MainComponent from './components/MainComponent/MainComponent.vue'

export default {
  name: 'App',
  components: {
    MainComponent
  }
}
</script>

<style>
.app {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
