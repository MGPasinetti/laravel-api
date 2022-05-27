<template>
    <div>
        <router-link :to="{ name: 'home'}">Home</router-link>
        <router-link :to="{ name: 'postIndex'}">blog</router-link>
        <router-link :to="{ name: 'about'}">about</router-link>
    </div>
</template>

<script>
export default {
    name: 'HeaderMain'
}
</script>

<style>
</style>
