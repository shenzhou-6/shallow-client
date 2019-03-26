<template>
    <a-layout>
        <shallow-header></shallow-header>
        <a-layout-content :style="{ margin: '24px 16px', padding: '24px', background: '#fff', minHeight: '280px' }">
            Content
        </a-layout-content>
    </a-layout>
</template>

<script>
    import ShallowHeader from "./ShallowHeader";
    export default {
        name: "ShallowContent",
        components: {ShallowHeader}
    }
</script>

<style scoped>

</style>