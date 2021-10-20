<template>
  <div id="logo">
    <router-link style=text-decoration:none; to="/">Eye<br>Cheatrace.</router-link>
  </div>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#logo {
  padding: 30px;
  text-align:left;
  font-size:30px;
  font-weight: bold;
  color: #000000;
}

#logo a {
  color: #000000;
}

body{
  background-image: url('./assets/background.png');
  background-size:100%;
}
</style>
