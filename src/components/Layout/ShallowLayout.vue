<template>
    <a-layout class="layout">
        <shallow-siderbar></shallow-siderbar>
        <shallow-content></shallow-content>
    </a-layout>
</template>

<script>
    import ShallowSiderbar from "./ShallowSiderbar";
    import ShallowContent from "./ShallowContent";
    export default {
        name: "ShallowLayout",
        components: {ShallowContent, ShallowSiderbar}
    }
</script>

<style scoped>
.layout{
    height: 100%;
}
</style>