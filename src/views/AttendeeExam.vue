<template>
  <div class="attendee">
    <div id="info">
        <h1>당신은 응시자입니다.</h1>
        <h1>👩‍💻{{sid}}</h1>
        <h1>🔗{{link}}</h1>
    </div>
  </div>
  <div class="monitors">
  </div>
  <div id="finishbtn">
    <button type="button" class="finish" @click="goToHome">시험종료</button>
  </div>
</template>

<script>
export default {
  name: 'Attendee',
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
  font-size:30px;
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
}
button:hover{
    color:black;
    background-color:white;
}
</style>