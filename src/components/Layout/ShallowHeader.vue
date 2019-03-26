<template>
    <a-layout-header style="background: #fff; padding: 0">
        <a-row>
            <a-col :span="2">
                <a-icon
                        class="trigger"
                        :type="$store.state.layout_store.collapsed ? 'menu-unfold' : 'menu-fold'"
                        @click="()=> $store.state.layout_store.collapsed = !$store.state.layout_store.collapsed"
                />
            </a-col>
            <a-col :span="19"></a-col>
            <a-col :span="3">
                <a-dropdown>
                    <div class="profile">
                        <a-avatar size="large" class="avatar" src="https://preview.pro.loacg.com/avatar2.jpg" />
                        <span>然后变成一只猫</span>
                    </div>
                    <a-menu slot="overlay" @click="onClick">
                        <a-menu-item key="center">
                            <a-icon type="user" />
                            <!--
                                                        <router-link :to="{name:'center'}"></router-link>
                            -->
                            <span>个人中心</span>
                        </a-menu-item>

                        <a-menu-item key="setting">
                            <a-icon type="setting" />
                            <span>网站设置</span>
                        </a-menu-item>
                        <a-menu-divider />
                        <a-menu-item key="logout">
                            <a-icon type="logout" />
                            <span>退出登录</span>
                        </a-menu-item>
                    </a-menu>
                </a-dropdown>
            </a-col>
        </a-row>
    </a-layout-header>
</template>

<script>
    import ACol from "ant-design-vue/es/grid/Col";
    export default {
        name: "ShallowHeader",
        components: {ACol}
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
    .avatar{
        margin: 20px 8px 20px 0;
    }
</style>