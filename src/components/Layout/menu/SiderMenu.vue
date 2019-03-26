<template>
    <div>
        <a-menu
                :defaultSelectedKeys="['1']"
                :defaultOpenKeys="['2']"
                mode="inline"
                theme="dark"
                :inlineCollapsed="$store.state.layout_store.collapsed"
        >
            <template v-for="item in list">
                <a-menu-item v-if="!item.children" :key="item.key">
                    <router-link :to="{name:item.key}">
                        <a-icon :type="item.icon" />
                        <span>{{item.title}}</span>
                    </router-link>
                </a-menu-item>
                <sub-menu v-else :menu-info="item" :key="item.key"/>
            </template>
        </a-menu>
    </div>
</template>

<script>
    import SubMenu from './SubMenu'
    export default {
        name: "SiderMenu",
        components: {
            'sub-menu': SubMenu,
        },
        data () {
            return {
                collapsed: false,
                list: [
                    {
                        key: '1',
                        title: 'Option 1',
                        icon:''
                    }, {
                        key: '2',
                        title: 'Navigation 2',
                        icon:'',
                        children: [
                            {
                                key: '2.1',
                                title: 'Navigation 3',
                                children: [
                                    { key: '2.1.1',
                                        title: 'Option 2.1.1',
                                    },
                                ],
                            },
                        ],
                    }],
            }
        },
    }
</script>

<style scoped>

</style>