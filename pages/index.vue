<template>
    <div>
        <h1>Danh sách công việc</h1>

        <ul>
            <li v-for="todo in data">
                {{ todo.title }}
                <nuxt-link :to="'/todo/' + todo.id" + todo.id
                    >Chi tiết</nuxt-link
                >
            </li>
        </ul>
    </div>
</template>

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
</script>
