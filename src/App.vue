<template>
  <div>
    <Header title="Schedule" message="CRUD of contacts with vue using components, watch, life cycle"></Header>
    <form-contact v-bind:contacts="contacts"></form-contact>

    <ListContact v-bind:contacts="contacts"></ListContact>
  </div>
</template>

<script>
import Form from './components/Form.vue'
import Header from './components/Header.vue'
import ListContact from './components/ListContact.vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'font-awesome/css/font-awesome.css'

export default {
  name: 'app',
  data(){
    return{
      contacts: []
    }
  },
  components:{
    'form-contact': Form,
     Header,
     ListContact
  }
}
</script>
