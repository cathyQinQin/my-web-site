<template>
  <Navigator/>
  <Introduction/>
  <AboutMe/>
</template>

<script>
import Navigator from './components/Navigator.vue'
import Introduction from './components/Introduction.vue'
import AboutMe from './components/AboutMe.vue'
export default {
  name: 'App',
  components: {
    Navigator,
    Introduction,
    AboutMe,
  }
}
</script>

<style>
#app {
  color: #666;
}
a {
  color: #666;
  cursor: hand;
  text-decoration: none;
}
ul{
  list-style: none;
}
</style>
