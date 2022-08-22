<script>
export default{
  data(){
    return{
      massage:"Helloworld",
      age:0
    }; 
  },
  computed:{//計算屬性 可直接使用
  reversMsg:function(){
    return this.massage.split('').reverse().join('')
  }

  },
  method:{
 reversMsg2:function(){
    return this.massage.split('').reverse().join('')
  }
  },
};
 

</script>

<template>
<p>{{massage}}</p>
<!-- 第一種 -->
<p>{{massage.split('').reverse().join('')}}</p>
<!-- 第二種 -->
<p>{{reversMsg}}</p>
<!-- 第三種 -->
<p>{{reversMsg2()}}</p>
<p></p>
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


</style>
