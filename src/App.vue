<template>
  <div id="app">
    <TopBar />
    <HelloWorld />
  </div>
</template>

<script>
import contact from './components/pop.vue'
import HelloWorld from './components/HelloWorld.vue';
import TopBar from './components/TopBar.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    contact,
    TopBar
  }
};
</script>

<style>
body{
    background: #011627;
}
#app {
  font-family: Arial, Helvetica, sans-serif;
 
}
</style>
