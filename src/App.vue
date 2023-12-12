<template>
  <h1 class="projectname">Vue Book Project</h1>
  <h1><a href="https://neacodes.com/" rel="home">NEA codes</a></h1>
  <SignUp/>
</template>

<script>

import SignUp from './components/SignUp.vue'
export default {
  name: 'App',
components: {
  SignUp
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.projectname{
  
    border: 1px solid darkblue;
border-radius: 8px 0px;
background-color: darkblue;
color: white;
}
</style>
