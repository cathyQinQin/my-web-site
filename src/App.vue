<template>
  <Navigator msg="Welcome to Your Vue.js App"/>
  <Introduction/>
</template>

<script>
import Navigator from './components/Navigator.vue'
import Introduction from './components/Introduction.vue'
export default {
  name: 'App',
  components: {
    Navigator,
    Introduction,
  }
}
</script>

<style>
#app {
  font-family: Apercu,sans-serif;
  text-align: center;
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
