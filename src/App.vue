<template>
  <!-- 모달 -->
  <div class="black-bg" v-if="modalWrap == true" >
    <div class="white-bg">
      <h4>상세페이지 제목1</h4>
      <p>상세페이지 내용</p>
      <button @click="modalWrap = false">닫기</button>
    </div>
  </div>
  <!-- 메뉴 -->
  <div class="menu">
    <a href="#" v-for="menuList in menuName" :key="menuList">{{menuList}}</a>
    <!-- <a href="#" v-for="(a,i)) in menuName" :key="i">{{i}}</a> -->
  </div>
  <!-- <div>
    <h4>{{product[0]}} 원룸</h4>
    <p>{{price[0]}} 만원</p>
  </div>
  <div>
    <h4>{{product[1]}} 원룸</h4>
    <p>{{price[1]}} 만원</p>
  </div>
  <div>
    <h4>{{product[2]}} 원룸</h4>
    <p>{{price[2]}} 만원</p>
  </div> -->
  <!-- <div v-for="(roomList,i) in 3" :key="i">
    <h4>{{product[i]}} 원룸</h4>
    <p>{{price[i]}} 만원</p>
  </div> -->
  <!-- <div v-for="(roomList,i) in product" :key="i">
    <h4>{{roomList}} 원룸</h4>
    <p>{{price[i]}} 만원</p>
  </div> -->
  <!-- <div>
    <h4 :style="txtRed">{{product[0]}} 원룸</h4>
    <p>{{price[0]}} 만원</p>
    <button @click="increase">허위매물신고</button> <span>신고수 : {{Num}}</span>
  </div>
  <div>
    <h4>{{product[1]}} 원룸</h4>
    <p>{{price[1]}} 만원</p>
    <button @click="Num++">허위매물신고</button> <span>신고수 : {{Num}}</span>
  </div>
  <div>
    <h4>{{product[2]}} 원룸</h4>
    <p>{{price[2]}} 만원</p>
  </div> -->
  <!-- <div>
    <h4 :style="txtRed">{{product[0]}} 원룸</h4>
    <p>{{price[0]}} 만원</p>
    <button @click="Num[0]+=100">허위매물신고</button> <span>신고수 : {{Num[0]}}</span>
  </div>
  <div>
    <h4>{{product[1]}} 원룸</h4>
    <p>{{price[1]}} 만원</p>
    <button @click="Num[1]++">허위매물신고</button> <span>신고수 : {{Num[1]}}</span>
  </div>
  <div>
    <h4>{{product[2]}} 원룸</h4>
    <p>{{price[2]}} 만원</p>
    <button @click="Num[2]++">허위매물신고</button> <span>신고수 : {{Num[2]}}</span>
  </div> -->
  <!-- <div v-for="(roomList,i) in 3" :key="i">
    <h4>{{product[i]}} 원룸</h4>
    <p>{{price[i]}} 만원</p>
    <button @click="Num[i]+=100">허위매물신고</button> <span>신고수 : {{Num[i]}}</span>
  </div> -->
  <div>
    <img src="./assets/room0.jpg" class="room-img">
    <h4 :style="hands" @click="modalWrap = true">{{product[0]}} 111원룸11</h4>
    <p>{{price[0]}} 만원</p>
    <button @click="Num[0]+=100">허위매물신고</button> <span>신고수 : {{Num[0]}}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{product[1]}} 원룸</h4>
    <p>{{price[1]}} 만원</p>
    <button @click="Num[1]++">허위매물신고</button> <span>신고수 : {{Num[1]}}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" class="room-img">
    <h4>{{product[2]}} 원룸</h4>
    <p>{{price[2]}} 만원</p>
    <button @click="Num[2]++">허위매물신고</button> <span>신고수 : {{Num[2]}}</span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      modalWrap : false,
      product: ['강남구','강북구','마포구'],
      price: [100,200,300],
      menuName: ['Home','About','Room','Board12'],
      Num: [0,0,0],
      txtRed: 'color:red',
      hands: 'cursor:pointer',
    }
  },
  methods: {
    increase(){
      this.Num++;
    }
  },
  components: {
  }
}
</script>

<style>
  body{text-align:center;margin:0;}
  div{box-sizing:border-box;}
  .menu{background:#336699;padding:15px;border-radius:5px;}
  .menu a{color:#fff;padding:15px;}
  .menu a:hover{color:yellow;}
  .room-img{width:100%;margin-top:40px;}
  .black-bg{position:fixed;width:100%;height:100%;padding:20px;background:rgba(0,0,0,0.5);}
  .white-bg{width:100%;background:#fff;border-radius: 8px;padding:20px;}
</style>
