<template>
  <div>
    <div id="app">
      <div id="top">
        <h4>게시판</h4>
        <p @click="모달창열렸니 = true">게시판 안내</p>
      </div>
    </div>

    <div class="black-bg" v-if="모달창열렸니==true">
      <div class="white-bg">
        <h4>게시판 사용 주의사항</h4>
        <p>{{게시판공지사항[0]}} {{게시판공지사항[1]}}</p>
        <button @click="모달창열렸니 = false"> 닫기 </button>
      </div>
    </div>

    <search/>

    <List :게시판="게시판" />

    <div class="black-bg" v-if="모달창열였다==true">
      <div class="white-bg">
        <p v-for="(a,i) in 게시판" :key="i" 누른거 = "i">{{ a }}</p>
        <button @click="모달창열였다 = false"> 닫기 </button>
      </div>
    </div>

<!--    <div class="main">-->
<!--      <a v-for="(a,i) in 게시판" :key="i"><a @click="모달창열였다 = true">{{ a.id }}</a> <a @click="모달창열였다 = true">{{ a.writer }}</a> <a @click="모달창열였다 = true" >{{ a.title }}</a> <a @click="모달창열였다 = true">{{ a.date }}</a> <a @click="모달창열였다 = true">{{ a.view }}</a> <a @click="모달창열였다 = true">{{ a.like }}</a> </a>-->
<!--    </div>-->

  </div>
</template>

<script>

import data from './assets/data';
import search from "@/search";
import List from "@/components/List";

export default {
  name: 'App',
  data(){
    return{
      조회수 : 0,
      게시판 : data,
      좋아요 : 0,
      누른거 : 0,
      모달창열렸니 : false,
      모달창열였다 : false,
      게시판공지사항 : ['이상한 글 사용 금지','욕 금지'],
    }
  },
  components: {
    List,
    search
  },
  methods : {
    up(){
      this.좋아요 += 1;
    }
  },
}
</script>

<style>
.main {
  background: white;
  padding: 15px;
  border-radius: 5px;
}
.main a {
  color: black;
  padding: 10px;
}
body {
  margin : 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height:100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 50px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#top {
  text-align: center;
}
</style>
