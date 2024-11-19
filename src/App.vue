<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <div class="black-bg" v-if="모달창열렸니">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
      <button @click="모달창열렸니=false">닫기</button>
    </div>
  </div>

  <!--<div v-for="(a,i) in products" :key="i">
    <h4>{{a}}</h4>
    <p>가격은 아무거나</p>
  </div>-->

  <div>
    <h4 @click="모달창열렸니 = true">{{products[0]}}</h4>
    <p>50만원</p>
    <button @click="신고수[0]++">허위매물 신고</button>
    <span>신고수 : {{신고수[0]}}</span>
    <img src="./assets/room0.jpg" class="room">
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>50만원</p>
    <button @click="신고수[1]++">허위매물 신고</button>
    <span>신고수 : {{신고수[1]}}</span>
    <img src="./assets/room1.jpg" class="room">
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>50만원</p>
    <button @click="신고수[2]++">허위매물 신고</button>
    <span>신고수 : {{신고수[2]}}</span>
    <img src="./assets/room2.jpg" class="room">
  </div>

  <!-- <div v-for="(a,i) in products" :key="i">
    <h4>{{a}}</h4>
    <p>가격은 아무거나</p>
    <button @click="increase(i)">허위매물 신고</button>
    <span>신고수 : {{신고수[i]}}</span>
  </div> -->

 
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      모달창열렸니 : false,
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
body {
  margin : 0
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: #fff;
  padding: 20px;
}

.room {
  width: 100%;
  margin-top: 50px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
