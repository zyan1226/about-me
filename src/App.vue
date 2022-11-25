<template>
  <img src="./assets/beams.jpg" alt="" class="top-1/2 left-1/2 max-w-none -translate-x-1/2 
  -translate-y-1/2 w-full h-screen fixed" />
  <div id="grid" class="fixed inset-0 bg-center 
  [mask-image:linear-gradient(180deg,white,rgba(255,255,255,0))]">
  </div>
  <AboutMe />
</template>

<script>
import AboutMe from './pages/AboutMe.vue'

export default {
  name: 'App',
  components: {
    AboutMe
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#grid {
  background-image: url(./assets/grid.svg);
}

body {
  margin: 0;
  padding: 0;
}
</style>
