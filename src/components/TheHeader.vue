<script setup lang="ts">
var firstName = "Emerson";
var lastName = " Souza";
</script>

<template>
    <header class="header">
        {{ firstName  + lastName}}
    </header>
</template>

<style scoped>
.header{
    background-color: blue;
}
</style>