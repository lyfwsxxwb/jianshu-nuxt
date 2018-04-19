<template>
    <div class="sign">
        <!--logo-->
        <div class="logo">
            <nuxt-link to="/">
                <img src="~/assets/img/logo.png">
            </nuxt-link>
        </div>
        <!--主体部分-->
        <div class="main">
            <!--title-->
            <div class="title">
                <h4>
                    <nuxt-link class="active" to="/sign-in">
                        登录
                    </nuxt-link>
                    <b>·</b>
                    <nuxt-link to="/sign-up">
                        注册
                    </nuxt-link>
                </h4>
            </div>
            <!--form表单-->
            <div class="js-form">
                <form method="post">
                    <div class="input-prepend">
                        <input type="text" placeholder="手机号或邮箱">
                        <i class="fa fa-user"></i>
                    </div>
                    <div class="input-prepend" id="sign-in-ps">
                        <input type="text" placeholder="密码">
                        <i class="fa fa-lock"></i>
                    </div>
                    <div class="remember">
                        <input type="checkbox" checked>
                        <span>记住我</span>
                    </div>

                        <nuxt-link class="help" to="/">登录遇到问题</nuxt-link>


                    <button class="sign-in-btn">登录</button>
                </form>
            </div>
            <!--第三方的登录-->
            <div class="more-sign">
                <p>社交账号登录</p>
                <ul>
                    <li class="weibo">
                        <nuxt-link to="/">
                            <i class="fa fa-weibo"></i>
                        </nuxt-link>
                    </li>
                    <li class="weixin">
                        <nuxt-link to="/">
                            <i class="fa fa-weixin"></i>
                        </nuxt-link>
                    </li>
                    <li class="qq">
                        <nuxt-link to="/">
                            <i class="fa fa-qq"></i>
                        </nuxt-link>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        //修改当前页面的默认模板为sign.vue
        //如果不写的话，默认是default.vue
        layout:'sign',
        //设置页面的标题以及描述、关键字等元信息
        head: {
            title: '登录-简书',
            meta: [
                {charset:'utf-8'},
                {name: 'keywords', content: '登录页面'},
                {name: 'description', content: '登录简书'},
                {name: 'author', content: 'MS xu'}
            ]
        },
        data() {
            return {}
        }
    }
</script>

