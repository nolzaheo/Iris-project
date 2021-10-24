<template>
  <div class="attendee">
    <div id="info">
        <h1>당신은 응시자입니다.</h1>
        <h1>👩‍💻 {{sid}}<br>🔗 {{link}}</h1>
    </div>
  </div>
  <div id="monitors">
    <video id="localVideo" autoplay muted playsinline></video>
    <video id="remoteVideo" autoplay playsinline></video>
  </div>
  <div id="finishbtn">
    <button type="button" class="finish" @click="goToHome">시험종료</button>
  </div>
</template>

<script>
export default {
  name: 'Attendee',
  data(){
    return{
      sid:'None',
      link:'None'
    }
  },
  mounted(){
    this.sid=this.$route.params.sid;
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
    position:fixed;
    bottom:30px;
    right:20px;
}
button:hover{
    color:black;
    background-color:white;
}
video {
  max-width: 100%;
  width: 320px;
}

</style>