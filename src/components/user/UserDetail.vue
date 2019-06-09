<template>
<div>
    <h3>Some User Details</h3>
    <p> Loaded item : {{ $route.params.id }}</p>
    <router-link tag="button" class="btn btn-primary" :to="{ name: 'userEdit', params: {id:$route.params.id}, query : { locale: 'en', q:100 } }">Edit User</router-link>
</div>
</template>

<script>
export default {
    beforeRouteEnter( to, from, next ) {
        if(true) {
            next();
        }
        else{
            next(false);
        }
    }
}
</script>
