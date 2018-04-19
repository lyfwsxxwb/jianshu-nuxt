<template>
    <div>
        <nav class="navbar navbar-fixed-top">
            <div class="width-limit">
                <!--logo-->
                <nuxt-link class="logo" to="/">
                    <img src="~/assets/img/navlogo.png">
                </nuxt-link>
                <!--右上角，写文章-->
                <nuxt-link to="/write" class="write-btn">
                    <i class="fa fa-edit"></i>
                    写文章
                </nuxt-link>
                <!--登录用户信息-->
                <div class="user" @mouseleave="leaveHandle">
                    <div class="drop-down" @mouseenter="enterHandle">
                        <nuxt-link to="/u123" class="avatar">
                            <img src="~/assets/img/default-avatar.jpg">
                        </nuxt-link>
                    </div>
                    <ul class="drop-menu" v-show="isShow">
                        <li>
                            <nuxt-link to="/u/123">
                                <i class="fa fa-home fa-fw"></i>
                                我的主页
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/users/123/like">
                                <i class="fa fa-heart fa-fw"></i>
                                喜欢的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/bookmarks">
                                <i class="fa fa-bookmark fa-fw"></i>
                                收藏的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/settings/basic">
                                <i class="fa fa-cog fa-fw"></i>
                                设置
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/logout">
                                <i class="fa fa-sign-out fa-fw"></i>
                                退出
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <!--右上角，登录和注册-->

            </div>
        </nav>
    </div>
</template>

<script>
    export default {
        name: "myHeader",
        data() {
            return {
                isShow: false
            }

        },
        methods: {
            enterHandle() {
                this.isShow = true;
            },
            leaveHandle() {
                this.isShow = false;
            }
        }

    }
</script>

<style scoped>
    nav {
        width: 100%;
        height: 56px;
    }

    .navbar {
        margin-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
        background-color: #fff;
    }

    .navbar:before {
        content: '';
        display: table;
    }

    .navbar-fixed-top {
        position: fixed;
        left: 0;
        top: 0;
        z-index: 9999;
    }

    nav .width-limit {
        min-width: 768px;
        max-width: 1440px;
        margin: 0 auto;

    }

    nav .logo {
        float: left;
        height: 56px;
        display: block;
    }

    nav .logo img {
        height: 100%;
    }

    nav .write-btn {
        float: right;
        width: 100px;
        height: 40px;
        line-height: 40px;
        margin: 8px 15px 0;
        border-radius: 20px;
        font-size: 15px;
        color: #fff;
        background: #ea6f5a;
        text-align: center;
    }

    nav .write-btn:hover {
        background: #ec6149;
        cursor: pointer;
    }

    nav .user {
        position: relative;
        float: right;

    }

    nav .user:hover {
        background-color: #f5f5f5;
    }

    nav .user .avatar {
        position: relative;
        display: block;
        width: 40px;
        height: 40px;
        margin: 8px 28px 8px 20px;
    }

    nav .user .avatar:before {
        content: '';
        position: absolute;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-top: 5px solid #999;
        top: 18px;
        right: -14px;
    }

    nav .user .avatar img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        border: 1px solid #ddd;
    }

    nav .user .drop-menu {
        position: absolute;
        left: 0;
        box-shadow: 0 0 8px rgba(0, 0, 0, .1);
        font-size: 15px;
        min-width: 160px;
        z-index: 999;
        margin: 0;
        padding: 10px 0;
        background: #fff;

    }

    nav .user .drop-menu li a {
        padding: 10px 20px;
        display: block;
        line-height: 30px;
    }

    nav .user .drop-menu li a:hover {
        background-color: #f5f5f5;
    }

    nav .user .drop-menu li a i {
        margin-right: 15px;
        color: #ea6f5a;
        /*下面两句话跟在上面i的class里面加fa-fw是一个效果*/
        /*width: 20px;*/
        /*heigth: 20px;*/
        font-size: 20px;
    }

</style>