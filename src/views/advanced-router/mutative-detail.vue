<template>
    <div>
        <basic-container>
            <el-tag type="success">动态路由接受参数{{$route.params}}</el-tag>
        </basic-container>
        <basic-container>
            <el-button type="primary"
                       @click="breaks">关闭返回列表</el-button>
        </basic-container>
    </div>
</template>

<script>
export default {
    methods: {
        breaks () {
            this.$router.$avueRouter.closeTag();
            this.$router.push({ path: '/advanced-router/mutative-router' })
        }
    }
};
</script>

<style>
</style>
