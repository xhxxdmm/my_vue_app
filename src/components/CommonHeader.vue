<template>
    <div class="header-container">
        <div class="l-content">
            <el-button @click="handleMenu" icon="el-icon-menu" size="mini"></el-button>
            <!-- 面包屑 -->
            <span class="text">首页</span>
        </div>
        <div class="r-content">
            <el-dropdown>
                <span class="el-dropdown-link">
                    <img class="user" src="..\src\assets\user.png" alt="">
                </span>
                <el-dropdown-menu slot="dropdown">
                    <el-dropdown-item>个人中心</el-dropdown-item>
                    <el-dropdown-item>退出</el-dropdown-item>
                </el-dropdown-menu>
            </el-dropdown>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {

            }
        },
        methods: {
            handleMenu(){
                this.$store.commit('collapseMenu')
            }
        },
    }
</script>

<style lang="less" scoped>
    .header-container {
        padding: 0 20px;
        background-color: #333;
        height: 60px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .l-content{
        span{
            color: #ffffff;
            margin-left: 20px;
        }
    }
    .r-content {
        .user {
            width: 40px;
            height: 40px;
            border-radius: 50%;
        }

    }
</style>