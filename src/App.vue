<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div v-for="(a,i) in products" :key="i">
    <h4>{{a}}</h4>
    <p>가격은 아무거나</p>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      products : ['역삼동원룸', '천호동원룸', '마포구원룸']
     }
  },
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
