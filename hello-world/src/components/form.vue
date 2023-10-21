<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form @submit="submitForm">
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
    <div>
      <label for="isDisable">Is disabled</label>
      <input type="checkbox" id="isDisable" v-model="formValues.isDisable">
    </div>
    <div><button>submit</button></div>
  </form>
</template>
   
   
<script>
export default {
  name: 'form-component',
  data() {
    return {
      formValues: {
        name: '',
        lastname: '',
        email: '',
        isDisable: false,
      }
    }
  },
  methods: {
    submitForm(event) {
      event.preventDefault()
      console.log('form values', this.formValues)
    }
  },
}


</script>
   
<style scoped>
div{
  padding: 5px;
  margin: 5px;

}

form {
  display: flex;
  justify-content: flex-start;
  flex-direction: column;
}
</style>
   