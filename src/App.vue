<template>
  <Navigator/>
  <Introduction/>
  <AboutMe/>
  <Project/>
  <Footer/>
</template>

<script>
import Navigator from './components/Navigator.vue'
import Introduction from './components/Introduction.vue'
import AboutMe from './components/AboutMe.vue'
import Project  from './components/Project.vue'
import Footer  from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    Navigator,
    Introduction,
    AboutMe,
    Project,
    Footer,
  }
}
</script>

<style>
*{
  margin:0;
  padding:0;
  border:0;
}
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
