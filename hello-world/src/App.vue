<template>
  <div>
  <div>{{ name }}</div>
  <div v-text="lastname"></div>
  <div v-text="email"></div>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      name:'Yusuf',
      lastname:'ELIK',
      email: 'ysfelik1@gmail.com',
    }
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
</style>
