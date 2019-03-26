<template>
    <a-layout-sider :trigger="null"
                    collapsible
                    v-model="$store.state.layout_store.collapsed">
        <div class="logo"></div>
        <sider-menu></sider-menu>
    </a-layout-sider>
</template>

<script>
    import ALayoutSider from "ant-design-vue/es/layout/Sider";
    import SiderMenu from "./menu/SiderMenu";
    export default {
        name: "ShallowSiderbar",
        components: {SiderMenu, ALayoutSider}
    }
</script>

<style scoped>
    .logo {
        height: 32px;
        background: rgba(255,255,255,.2);
        margin: 16px;
    }

</style>