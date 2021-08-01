<template>

    <el-menu
            class="el-menu-vertical-demo"
            active-text-color="#ffdd44"
            router
    >

        <MenuList :list="menuList"></MenuList>

    </el-menu>
</template>

<script>
    import MenuList from "./MenuList";

    export default {
        name: "Menu",
        components: {MenuList},
        data(){
            return {
                menuList: [
                    {
                        title: '首页',
                        name: 'index',
                        icon: 'el-icon-s-home',
                        path: '/index',
                        children: []
                    },
                    {
                        title: '系统管理',
                        name: 'SysManege',
                        icon: 'el-icon-s-operation',
                        path: 'sysMange',
                        children: [
                            {
                                title: '用户管理',
                                name: 'SysUser',
                                icon: 'el-icon-s-custom',
                                path: '/sys/user',
                                children: []
                            }
                        ]
                    },
                    {
                        title: '系统工具',
                        name: 'SysTools',
                        icon: 'el-icon-s-tools',
                        path: 'sysTools',
                        children: [
                            {
                                title: '数字字典',
                                name: 'SysDict',
                                icon: 'el-icon-s-order',
                                path: '/sys/dict',
                                children: []
                            }
                        ]
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    .el-menu-vertical-demo{
        height: 100vh;
    }
</style>
