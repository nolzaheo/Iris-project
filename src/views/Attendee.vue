<template>
  <div class="attendee">
    <h1>Welcome, Attendee!👋</h1>
    <div>
      <label>👩‍💻</label>
      <input class="inputsid" v-model="inputsid" placeholder="input sID">
    </div>
    <div>
      <label>🔗</label>
      <input class="inputlink" v-model="inputlink" placeholder="input link">
    </div>
    <div>
      <button type="button" class="inputenter" @click="goToAttendeeExam">입장하기</button>
    </div>
    
    <!--h1>{{inputlink}}</h1>
    <h1>{{inputsid}}</h1-->
    
  </div>
</template>
<script>
  export default {
    name:'attendee',
    data(){
      return{
          inputsid:'',
          inputlink:'',
      }
    },
    methods:{
      goToAttendeeExam(){
        this.$router.push({path:'/attendee/exam/'+this.inputsid+'/'+this.inputlink});
      }
    }
  }
</script>
<style scoped>
  *{
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-weight: bold;
  }
  input{
    width: 15%;
    height: 20px;
    border-radius: 20px;
    border: 1px;
    margin: 8px 0;
    padding: 8px 12px;
    background-color:rgba( 255, 255, 255, 0.5 );
    font-size:15px;
    color:#2c3e50;
  }
  input::placeholder{
    color:#c7c7c7;
  }
  button{
    width: 230px;
    height:50px;
    background-color:black;
    color:white;
    font-size:20px;
    font-weight: bold;
    border-radius:48px;
    border:0px;
    margin:10px;
  }
  button:hover{
    color:black;
    background-color:white;
  }
  label{
    font-size:25px;
    margin-right:5px;
  }
</style>

