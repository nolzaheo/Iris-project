<template>
  <div class="home">
    <div id=buttons>
      <div>
        <button type="button" class="attendee" @click="goToAttendee">응시자</button>
      </div>
      <div>
        <button type="button" class="inspector" @click="goToInspector">감독관</button>
      </div>
    </div>
  </div>
</template>

<script>
var link='link4test'
export default {
  name: 'Home',
  data(){
      return{
          link:'1234'
      }
    },
  methods:{
      goToAttendee(){
        this.$router.push({path:'/attendee'});
      },
      goToInspector(){
        this.$router.push({path:'/inspector/'+link});
      }
    }
}
</script>
<style scoped>
  #Home {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
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
  }
  button:hover{
    color:black;
    background-color:white;
  }
  #buttons{
    position:relative;
    top:200px;
  }
  
</style>
