<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues,null,2) }}
    </pre>
  </div>
    <form>
        <div>
          <label for="name">Name</label>
          <input type="text" id="name" v-model="formValues.name">
        </div>
        <div>
          <label for="lastname">Lastname</label>
          <input type="text" id="lastname" v-model="formValues.lastname">
        </div>
         <div>
          <label for="email">Email</label>
          <input type="email" id="email" v-model="formValues.email">
        </div>
    </form>
  
</template>
   
   
<script>
export default {
  name: 'form-component',
  data(){
    return{
      formValues:{
        name:'',
        lastname:'',
        email:'',
      }
    }
    },
    methods:{

    },
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
   