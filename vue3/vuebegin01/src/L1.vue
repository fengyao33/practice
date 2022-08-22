<script>
// vue是聲明式宣染
export default{
  data(){
    return{
      num:0,
      uname:"me",
      mag:"<h2>標籤<h2>",
      id:"d1",
      改變圖片:"https://gw.alicdn.com/i4/2206525179166/O1CN01AnMUvb2Ha52Z1pGX7_!!0-item_pic.jpg_Q75.jpg_.webp",
      attributeN:"id",
      mouseEvent:"click"
    };
  },
  methods:{
    // vue定義方法
    changeN:function(){
      this.uname="李四"
    }
  }
}

</script>

<template>
<div>
 <p>{{num}}{{uname}}</p>
 <!-- v-once 指令 數值改變不更新 -->
 <p v-once>{{uname}}</p>
 <button @click="changeN">改變名子</button>
<p>{{msg}}</p>
<!-- v-html 變更html 很危險 xxs攻擊 -->
<p v-html=mag></p>
<!-- -v-bind: 綁定ID  改變屬性內容 -->
<p v-bind:id="id">v-bind綁定</p>
<img v-bind:src="改變圖片" alt="">
<!-- 使用JS表達式 -->
<p>{{num+1}}</p>
<p>{{uname.split('').reverse().join('')}}</p>
<p v-bind:id="id+1">v-bind綁定</p>
<!-- id改變成d11 -->
<!-- 語法糖 兩個相同 -->
<p v-bind:id="id">v-bind綁定</p>
<p :id="id">v-bind綁定</p>
<!-- v-on = @   語法糖 -->
 <button @click="changeN">改變名子</button>
 <button v-on:click="changeN">改變名子</button>
 <!-- 動態參數 [] -->
<p v-bind:[attributeN]="id">v-bind綁定</p>
<button @click="attributeN='class'">改變屬性</button>
<!-- 動態事件 -->
<button @[mouseEvent]="attributeN='class'">改變屬性</button>
<button @clicl="mouseEvent=mouseover">變over事件</button>






</div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#d1{
  color: aquamarine;
}
.d1{
  font-size: 50px;}
</style>
