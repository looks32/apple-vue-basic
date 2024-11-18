<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div>
    <h4 :style="스타일">원룸</h4>
    <p>{{price1}} 만원</p>
    <!-- asds -->
  </div>
  <div>
    <h4>원룸</h4>
    <p>{{price2}} 만원</p>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      price1 : 60,
      price2 : 50,
      스타일 : 'color : blue'
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
  margin-top: 60px;
}
</style>
