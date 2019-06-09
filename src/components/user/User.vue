<template>
<div>
    <h1>The User Page</h1>
    <hr>
    <router-view></router-view>
    <hr>
    <button class="btn btn-primary" @click="navigate">Go To Home</button>
</div>
</template>

<script>
export default {
    data() {
        return {
        }
    },
    methods: {
        navigate() {
            this.$router.push("/");
        }
    },
}
</script>
