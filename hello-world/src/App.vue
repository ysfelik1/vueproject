<template>
  <!--  <div v-bind:id="customerId">
    <div>{{ name }}</div>
    <div v-text="lastname"></div>
    <div v-text="email"></div>
    <button v-bind:disabled="isDisable">select</button>
  </div>
  -->
  <div class="list" v-for="customer in customersList" :key="customer.customerId">
    <div>{{ customer.name }}</div>
    <div v-text="customer.lastname"></div>
    <div v-text="customer.email"></div>
    <button v-bind:disabled="customer.isDisable">select</button>\
    <button v-on:click="selectCustomer(customer.customerId)">select</button>

  </div>
  <FormComponent />
    <!--<DetailsComponent customerId={{ this.selectedId}}/> -->
  <DetailsComponent :customerId="selectedId"/>

</template>


<script>
import FormComponent from './components/form.vue';
import DetailsComponent from './components/DetailsComponent.vue'
export default {

  name: 'App',
  components: {
    FormComponent,
    DetailsComponent,
  },
  data() {
    return {
      selectedId: null,
      customersList: [{
        customerId: '1',
        name: 'Yusuf',
        lastname: 'ELIK',
        age: 34,
        email: 'ysfelik1@gmail.com',
        isDisable: false,
      }
        ,
      {
        customerId: '2',
        name: 'John',
        lastname: 'Doe',
        age: 55,
        email: 'jdoe@gmail.com',
        isDisable: false,
      }
        ,
      {
        customerId: '3',
        name: 'Elon',
        lastname: 'Musk',
        age: 54,
        email: 'emusk@gmail.com',
        isDisable: false,
      }
        ,
      {
        customerId: '4',
        name: 'Bill',
        lastname: 'Gates',
        age: 64,
        email: 'bgates@gmail.com',
        isDisable: false,
      }
      ]
    }
  },
  methods: {
    selectCustomer(customerId) {
      this.selectedId=customerId;
      console.log( this.selectedId);
    }
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

.list {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 1rem;
  margin: 1rem;

}

.list div {
  padding: 1rem 1rem;
}</style>
