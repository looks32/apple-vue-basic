<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <!--<div v-for="(a,i) in products" :key="i">
    <h4>{{a}}</h4>
    <p>가격은 아무거나</p>
  </div>-->

  <!-- <div>
    <h4>{{products[0]}}</h4>
    <p>50만원</p>
    <button @click="increase(i)">허위매물 신고</button>
    <span>신고수 : {{신고수[0]}}</span>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>50만원</p>
    <button @click="increase(i)">허위매물 신고</button>
    <span>신고수 : {{신고수[1]}}</span>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>50만원</p>
    <button @click="increase(i)">허위매물 신고</button>
    <span>신고수 : {{신고수[2]}}</span>
  </div> -->

  <div v-for="(a,i) in products" :key="i">
    <h4>{{a}}</h4>
    <p>가격은 아무거나</p>
    <button @click="increase(i)">허위매물 신고</button>
    <span>신고수 : {{신고수[i]}}</span>
  </div>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      신고수 : [0, 0, 0],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸']
     }
  },
  methods : {
    increase(i){
      this.신고수[i]++;
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
