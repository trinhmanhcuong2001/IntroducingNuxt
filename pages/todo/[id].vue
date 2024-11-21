<script setup lang="ts">
const data = [
    {
        id: 1,
        title: "Quét nhà",
        completed: "Hoàn thành",
    },
    {
        id: 2,
        title: "Quét sân",
        completed: "Chưa hoàn thành",
    },
    {
        id: 3,
        title: "Lau nhà",
        completed: "Chưa hoàn thành",
    },
];
const route = useRoute();

const todo = data.find((t) => t.id === Number(route.params.id));
</script>
<template>
    <div v-if="todo">
        <h2>Trang chi tiết</h2>
        <h3>ID: {{ todo.id }}</h3>
        <p>Tiêu để : {{ todo.title }}</p>
        <p>Trạng thái: {{ todo.completed }}</p>
    </div>
    <nuxt-link to="/"><button>Quay lại</button></nuxt-link>
</template>
