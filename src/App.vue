<template>
  <div id="app">
    <my-header/>
    <router-view/>
    <my-footer/>
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42a7b9;
}
</style>
<script>
import myHeader from './components/myHeader.vue';
import myFooter from './components/myFooter.vue';
export default {
  name: 'App',
  components: {
    myHeader,
    myFooter
  },
}
</script>


