<template>
    <div class="container center-table">
    <table class="table table-responsive">
        <thead>
            <td>Index</td>
            <td>Name</td>
            <td>Phone</td>
            <td>#</td>
        </thead>
        <tbody>
            <tr v-for="(contact, index) in contacts" :key="contact">
                <td>{{index}}</td>
                <td>{{contact.name}}</td>
                <td>{{contact.phone}}</td>
                <td><button class="btn btn-danger" v-on:click="deleteContact(index)"><i class="fa fa-trash" /></button></td>
            </tr>
        </tbody>
    </table>
    </div>
</template>

<script>
    export default {
        name: 'ListContact',
        props: {
            contacts: [],        
        },
        methods: {
            deleteContact(index){
                this.contacts.splice(index, 1);
            }
        },
    }
</script>

<style>
.center-table{
    margin-top: 5%;    
}
</style>