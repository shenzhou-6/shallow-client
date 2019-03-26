<template>
    <a-layout-header style="background: #fff; padding: 0">
        <a-icon
                class="trigger"
                :type="$store.state.layout_store.collapsed ? 'menu-unfold' : 'menu-fold'"
                @click="()=> $store.state.layout_store.collapsed = !$store.state.layout_store.collapsed"
        />
    </a-layout-header>
</template>

<script>
    export default {
        name: "ShallowHeader"
    }
</script>

<style scoped>
    .trigger{
        font-size: 18px;
        line-height: 64px;
        padding: 0 24px;
        cursor: pointer;
        transition: color .3s;
    }
    .trigger:hover {
        color: #1890ff;
    }
</style>