<template>
  <div class="inspector">
    <div id="info">
      <h1>당신은 감독관입니다.</h1>
      <h1>🔗 {{link}}</h1>
    </div>
  </div>
  <div class="monitors">
  </div>
  <div>
    <button type="button" class="finish" @click="goToHome">시험종료</button>
  </div>
</template>

<script>
export default {
  name: 'Inspector',
  data(){
    return{
      link:'None'
    }
  },
  mounted(){
    this.link=this.$route.params.link;
  },
  methods:{
      goToHome(){
        this.$router.push({path:'/'});
      }
    }
}
</script>
<style scoped>
h1{
  text-align:left;
  margin-left:20px;
  font-size:25px;
  margin-top:2px;
}
button{
    width:190px;
    height:50px;
    margin:10px;
    background-color:black;
    color:white;
    font-size:20px;
    font-weight: bold;
    border-radius:48px;
    border:0px;
    margin:10px;
    position:fixed;
    bottom:30px;
    right:20px;
}
button:hover{
  color:black;
  background-color:white;
}
</style>