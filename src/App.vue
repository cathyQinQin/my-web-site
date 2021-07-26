<template>
  <Navigator/>
  <Introduction/>
  <AboutMe/>
  <Project/>
</template>

<script>
import Navigator from './components/Navigator.vue'
import Introduction from './components/Introduction.vue'
import AboutMe from './components/AboutMe.vue'
import Project  from './components/Project.vue'
export default {
  name: 'App',
  components: {
    Navigator,
    Introduction,
    AboutMe,
    Project,
  }
}
</script>

<style>
#app {
  color: #666;
  background: #fafafa;
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
