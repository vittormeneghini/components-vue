<template>
<div class="container text-center">       
    <h3>{{title}}</h3>
    <hr>
    <h6 class="text-secondary">{{message}}</h6>    
    <hr>
</div>
</template>

<script>
export default {
    name: 'Header',
    props: {
        title: String,
        message: String
    }
}
</script>