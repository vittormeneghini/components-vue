<template>
<div>   
    <form v-on:submit.prevent="submitForm">
        <div class="container">
        <div class="row">
            <div class="col-md">
            <input v-model="name" class="form-control" placeholder="Type name here" />
            </div>
            <div class="col-md">
            <input v-model="phone" class="form-control" placeholder="Type phone here" />
            </div>
            <button class="btn btn-success">Create</button>            
        </div>
        </div>
    </form>
</div>
</template>

<script>
    export default {
        name: 'Form',
        data(){
            return{
                name: '',
                phone: ''
            }
        },
        props:{
            contacts: []
        },
        methods: {
            submitForm(){
                this.contacts.push({'name': this.name, 'phone': this.phone})                
                this.name = ''
                this.phone = ''
            }
        },
    }
</script>