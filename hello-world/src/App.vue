<template>
  <div v-bind:id="customerId">
    <div>{{ name }}</div>
    <div v-text="lastname"></div>
    <div v-text="email"></div>
    <button v-bind:disabled="isDisable">select</button>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      customerId:'1',
      name:'Yusuf',
      lastname:'ELIK',
      email: 'ysfelik1@gmail.com',
      isDisable:false,
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
