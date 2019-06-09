<template>
<div>
    <h3>Edit the User</h3>
    <p>locale : {{ $route.query.locale }}</p>
    <p>analytics : {{ $route.query.q }}</p>
    <hr>
    <button class="btn btn-primary" @click="confirmed=true">Confirm</button>
</div>
</template>

<script>
export default {
    data() {
        return {
            confirmed : false
        }
    },
    beforeRouteLeave (to , from , next) {
        if(this.confirmed)
            next();
        else {
            if(confirm("Do you wanna leave"))
                next();
            else 
                next(false);
        }
    }
}
</script>
