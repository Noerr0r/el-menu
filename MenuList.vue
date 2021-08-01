<template>

    <div>
        <template v-for="(item) in list">

            <template v-if="item.children&&item.children.length>0">
                <el-submenu :index="item.path">
                    <template slot="title">
                        <i :class="item.icon"></i>
                        <span slot="title">{{item.title}}</span>
                    </template>

                    <MenuList :list="item.children"></MenuList>

                </el-submenu>
            </template>

            <template v-else>
                <el-menu-item :index="item.path" >
                    <template slot="title">
                        <i :class="item.icon"></i>
                        <span slot="title">{{item.title}}</span>
                    </template>
                </el-menu-item>
            </template>

        </template>

    </div>
</template>

<script>


    export default {
        name: "MenuList",
        props: ["list"] //Menu组件接受一个list作为菜单数据
    }

</script>

<style scoped>

</style>
