<script lang="ts" setup>
const handleMessage = () => {
    message.success("This is a normal message");
};
</script>
<template>
    <h1>Đây là trang {{ $route.params.id }} - {{ $route.params.job }}</h1>
    <a-button @click="handleMessage"> button </a-button>
</template>
