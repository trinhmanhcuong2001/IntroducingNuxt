<template>
    <a-layout style="min-height: 100vh">
        <a-layout-sider v-model:collapsed="collapsed" collapsible>
            <div class="logo" />
            <a-menu
                v-model:selectedKeys="selectedKeys"
                theme="dark"
                mode="inline"
            >
                <a-menu-item key="1">
                    <nuxt-link to="/">
                        <pie-chart-outlined />
                        <span>Dashboard</span>
                    </nuxt-link>
                </a-menu-item>
                <a-menu-item key="2">
                    <nuxt-link to="/dashboard/profile">
                        <desktop-outlined />
                        <span>Profile</span>
                    </nuxt-link>
                </a-menu-item>

                <a-menu-item key="3">
                    <nuxt-link to="/dashboard/settings">
                        <file-outlined />
                        <span>Settings</span>
                    </nuxt-link>
                </a-menu-item>
            </a-menu>
        </a-layout-sider>
        <a-layout>
            <a-layout-header style="background: #fff; padding: 0" />
            <a-layout-content style="margin: 0 16px">
                <!-- <a-breadcrumb style="margin: 16px 0">
                    <a-breadcrumb-item>User</a-breadcrumb-item>
                    <a-breadcrumb-item>Bill</a-breadcrumb-item>
                </a-breadcrumb> -->
                <div
                    :style="{
                        padding: '24px',
                        background: '#fff',
                        minHeight: '360px',
                    }"
                >
                    <slot />
                </div>
            </a-layout-content>
            <a-layout-footer style="text-align: center">
                Đây là footer
            </a-layout-footer>
        </a-layout>
    </a-layout>
</template>
<script lang="ts" setup>
const collapsed = ref<boolean>(false);
const selectedKeys = ref<string[]>(["1"]);
</script>
<style scoped>
#components-layout-demo-side .logo {
    height: 32px;
    margin: 16px;
    background: rgba(255, 255, 255, 0.3);
}

.site-layout .site-layout-background {
    background: #fff;
}
[data-theme="dark"] .site-layout .site-layout-background {
    background: #141414;
}
</style>
