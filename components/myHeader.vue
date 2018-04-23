<template>
    <div>
        <nav class="navbar navbar-fixed-top">
            <div class="width-limit">
                <nuxt-link to='/' class="logo">
                    <img src="~/assets/img/navlogo.png" alt="">
                </nuxt-link>
                <nuxt-link to='/write' class="write-btn">
                    <i class="fa fa-edit"></i>
                    写文章
                </nuxt-link>
                <div class="user" @mouseleave="dropOut(dropShow=false)">
                    <div class="drop-down" @mouseover="dropOver(dropShow=true)">
                        <nuxt-link to='/u/123' class="avator">
                            <img src="~/assets/img/default-avatar.jpg" alt="">
                        </nuxt-link>
                    </div>
                    <ul class="drop-menu" v-show="dropShow">
                        <li>
                            <nuxt-link to='/'>
                                <i class="fa fa-home fa-fw"></i>
                                我的主页
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to='/users/123/like'>
                                <i class="fa fa-heart fa-fw"></i>
                                喜欢的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to='/bookmarks'>
                                <i class="fa fa-bookmark fa-fw"></i>
                                收藏的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to='/settings/basic'>
                                <i class="fa fa-cog fa-fw"></i>
                                设置
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to='/logout'>
                                <i class="fa fa-sign-out fa-fw"></i>
                                退出
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <div class="container">
                    <transition name="fade">
                        <ul class="nav-list">
                            <li>
                                <nuxt-link to='/' class="active">
                                    <i class="fa fa-compass"></i>
                                    <span>发现</span>
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to='/'>
                                    <i class="fa fa-book"></i>
                                    <span>关注</span>
                                </nuxt-link>
                            </li>
                            <li @mouseover="messageShowHandle(messageShow=true)" @mouseleave="messageHideHandle(messageShow=false)" class="user">
                                <nuxt-link to='/'>
                                    <i class="fa fa-bell-o"></i>
                                    <span>消息</span>
                                </nuxt-link>
                                <ul class="drop-menu" v-show="messageShow">
                                    <li>
                                        <nuxt-link to='/'>
                                            <i class="fa fa-comment-o"></i>
                                            评论
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to='/'>
                                            <i class="fa fa-envelope-o"></i>
                                            简信
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to='/'>
                                            <i class="fa fa-square-o"></i>
                                            关注
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to='/'>
                                            <i class="fa fa-heart-o"></i>
                                            喜欢和赞
                                        </nuxt-link>
                                    </li>
                                </ul>
                            </li>
                            <li class="search">
                                <form method="post">
                                    <input type="text" placeholder="搜索" class="search-input">
                                    <a href="#" class="search-btn">
                                        <i class="fa fa-search"></i>
                                    </a>
                                </form>
                            </li>
                        </ul>
                    </transition>
                    <div class="navbar-header">
                        <button type="button" class="navbar-toggle" @click="slideToggle()">
                            <i class="fa fa-bars"></i>
                        </button>
                    </div>
                </div>
            </div>
        </nav>
    </div>
</template>
<script>
    export default {
        name: "myHeader",
        data() {
            return {
                dropShow: false,
                messageShow: false,
                menuShow: false,
                count: 0
            };
        },
        methods: {
            slideToggle() {
                this.count++;
                var count = this.count;
                var content = document.querySelector("nav .nav-list");
                content.style.transition = ".2s";
                if (count % 2 == 1) {
                    content.style.height = "224px";
                } else {
                    content.style.height = "0";
                }
            }
        }
    };
</script>
<style scoped>
    nav {
        width: 100%;
        height: 56px;
    }
    .navbar {
        margin-bottom: 20px;
        border-width: 0 0 1px;
        border-color: #f0f0f0;
        border-bottom: 1px solid #f0f0f0;
        position: relative;
    }
    .navbar:before {
        display: table;
        content: "";
    }
    .navbar-fixed-top {
        position: fixed;
        top: 0;
        left: 0;
        z-index: 10000;
    }
    nav .width-limit {
        min-width: 768px;
        max-width: 1440px;
        margin: 0 auto;
        height: 56px;
        /* background-color: black; */
    }
    nav .logo {
        float: left;
        height: 56px;
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
        background-color: #ea6f5a;
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
    nav .user .avator {
        position: relative;
        display: block;
        width: 40px;
        height: 40px;
        margin: 8px 10px 8px 25px;
        display: inline-block;
    }
    nav .user:hover {
        background-color: #f5f5f5;
    }
    nav .user .drop-menu li a:hover {
        background-color: #f5f5f5;
    }
    nav .user .avator:before {
        content: "";
        position: absolute;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-top: 5px solid #999;
        right: -14px;
        top: 18px;
    }
    nav .user .avator img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        border: 1px solid #ccc;
    }
    nav .user .drop-menu {
        box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
        position: absolute;
        left: 0;
        min-width: 160px;
        z-index: 10000;
        margin: 0;
        background: #fff;
        padding: 10px 0;
        font-size: 15px;
    }
    nav .user .drop-menu li a {
        padding: 10px 20px;
        display: block;
        line-height: 30px;
    }
    nav .user .drop-menu li a i {
        margin-right: 15px;
        color: #ea6f5a;
        font-size: 18px;
    }
    nav .nav-list {
        float: left;
    }
    nav .nav-list > li {
        float: left;
        margin-right: 5px;
    }
    nav .nav-list > li a {
        height: 56px;
        line-height: 26px;
        padding: 15px;
        display: block;
    }
    nav .nav-list > li a.active {
        color: #ea6f5a;
        background: none !important;
    }
    nav .nav-list > li a:hover {
        background-color: #f5f5f5;
    }
    nav .nav-list > li a i {
        margin-right: 5px;
        font-size: 20px;
    }
    nav .nav-list .drop-menu a i {
        color: #ea6f5a;
    }

    nav .nav-list::after {
        content: "";
        clear: both;
        display: block;
        height: 0;
        visibility: hidden;
    }
    nav .nav-list .search {
        padding-left: 15px;
        margin-right: 10px;
    }
    nav .nav-list .search form {
        margin-bottom: 20px;
        position: relative;
        top: 9px;
    }
    nav .nav-list .search form input {
        background: #eee;
        height: 38px;
        font-size: 14px;
        padding: 0 40px 0 20px;
        border: 1px solid #eee;
        border-radius: 40px;
        width: 240px;
    }
    nav .nav-list .search form input:focus {
        width: 320px;
        transition: 0.5s;
    }
    nav .nav-list .search form .search-btn {
        position: absolute;
        width: 30px;
        height: 30px;
        top: 2px;
        right: 5px;
        color: #969696;
        text-align: center;
        font-size: 15px;
        
        padding: 0;

    }
    nav .nav-list .search form .search-btn i {
        margin: 0;
        text-align: center;
        line-height: 40px;
        font-size: 15px;
        position: relative;
        top: -4px;
    }
    nav .nav-list .search form .search-btn:hover {
        background: none;
    }
    nav .nav-list .search form input:focus ~ .search-btn {
        background: #969696;
        border-radius: 50%;
        color: white;
    }
    nav .nav-list .search form input:focus ~ .search-btn i {
        padding-bottom: 2px;
    }

    nav .navbar-header .navbar-toggle {
        background-color: white;
        border: 1px solid #ddd;
        color: #969696;
        position: absolute;
        top: 7px;
        left: 100px;
        width: 43px;
        font-size: 25px;
        height: 43px;
        border-radius: 7px;
        display: none;
    }

    .fade-enter-active,
    .fade-leave-active {
        transition: all 0.5s;
    }

    .fade-enter,
    .fade-leave-to {
        transform: translateY(-20px);
        opacity: 0;
    }
    @media (max-width: 1440px) {
        nav .nav-list > li a > i {
            display: none;
        }
        nav .nav-list .search-btn i {
            display: inline-block;
        }
        nav .nav-list .search form .search-input {
            width: 160px;
        }
        nav .nav-list .search form .search-input:focus {
            width: 240px;
        }
    }
    @media (max-width: 1080px) {
        nav .nav-list li span {
            display: none;
        }
        nav .nav-list > li a i {
            display: block;
        }
    }

    @media (max-width: 768px) {
        nav .nav-list {
            overflow: hidden;
            height: 0;
        }
        nav .nav-list li span {
            display: block;
        }
        nav .nav-list > li a i {
            display: none;
        }
        nav .navbar-header .navbar-toggle {
            display: block;
        }
        nav .nav-list > li {
            width: 100%;
            text-align: center;
            border-bottom: 1px solid #ddd;
            display: block;
        }
        nav .nav-list {
            position: absolute;
            top: 56px;
            background-color: white;
            width: 100%;
        }
        nav .nav-list .search form .search-input {
            width: 90%;
        }
        nav .nav-list .search form .search-input:focus {
            width: 90%;
        }
        nav .nav-list .search form .search-btn {
            right: 40px;
        }
        nav .nav-list {
            border-bottom: 1px solid #ddd;
        }
        nav .nav-list .drop-menu {
            display: none;
        }
    }
    @media (min-width: 768px) {
        nav .nav-list > li a i {
            display: inline-block;
        }
    }
</style>

