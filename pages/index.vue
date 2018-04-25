<template>
    <div style="height: 100%;">
        <my-header></my-header>
        <div class="container index">
            <div class="row">
                <!--占16份-->
                <div class="col-xs-16 main">
                    <!--热门专题-->
                    <div class="recommend-collection">
                        <nuxt-link class="collection" to="/collection/123">
                            <img src="~assets/img/c_1.jpg">
                            <span name="name">手绘</span>
                        </nuxt-link>

                        <nuxt-link class="collection" to="/collection/123">
                            <img src="~assets/img/c_2.jpg">
                            <span name="name">读书</span>
                        </nuxt-link>

                        <nuxt-link class="collection" to="/collection/123">
                            <img src="~assets/img/c_3.jpg">
                            <span name="name">社会热点</span>
                        </nuxt-link>

                        <nuxt-link class="collection" to="/collection/123">
                            <img src="~assets/img/c_4.jpg">
                            <span name="name">@IT·互联网</span>
                        </nuxt-link>

                        <nuxt-link class="collection" to="/collection/123">
                            <img src="~assets/img/c_1.jpg">
                            <span name="name">旅行·在路上</span>
                        </nuxt-link>

                        <nuxt-link class="collection" to="/collection/123">
                            <img src="~assets/img/c_2.jpg">
                            <span name="name">历史</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123" class="more-collection">
                            更多热门专题
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                    <div class="split-line"></div>
                    <!--文章列表-->
                    <div class="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link to="/p/123" class="wrap-img">
                                    <img src="~assets/img/note.jpg">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/p/123" class="avatar">
                                            <img src="~assets/img/default-avatar.jpg">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="'/u/123" class="nickname">测试用户</nuxt-link>
                                            <span class="time">04.12 10:18</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">《芳华》--小萍，愿你被世界温柔以待</nuxt-link>
                                    <div class="abstruct">
                                        我已经很久不去电影院，但是《芳华》预告出来后，我一直很期待。虽然冯导上部《我不是潘金莲》让人略感失望，但他仍是我最喜爱的导演之一。 因为没有合适的同伴，我是一个人去看的。看的...
                                    </div>
                                    <div class="meta">
                                        <nuxt-link to="/c/123" class="collection-tag">社会与法</nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            1500
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            100
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            20
                                        </span>

                                    </div>
                                </div>

                            </li>
                            <li>

                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/p/123" class="avatar">
                                            <img src="~assets/img/default-avatar.jpg">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="'/u/123" class="nickname">测试用户</nuxt-link>
                                            <span class="time">04.12 10:18</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">《芳华》--小萍，愿你被世界温柔以待</nuxt-link>
                                    <div class="abstruct">
                                        我已经很久不去电影院，但是《芳华》预告出来后，我一直很期待。虽然冯导上部《我不是潘金莲》让人略感失望，但他仍是我最喜爱的导演之一。 因为没有合适的同伴，我是一个人去看的。看的...
                                    </div>
                                    <div class="meta">
                                        <nuxt-link to="/c/123" class="collection-tag">社会与法</nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            1500
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            100
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            20
                                        </span>

                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link to="/p/123" class="wrap-img">
                                    <img src="~assets/img/note.jpg">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/p/123" class="avatar">
                                            <img src="~assets/img/default-avatar.jpg">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="'/u/123" class="nickname">测试用户</nuxt-link>
                                            <span class="time">04.12 10:18</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">《芳华》--小萍，愿你被世界温柔以待</nuxt-link>
                                    <div class="abstruct">
                                        我已经很久不去电影院，但是《芳华》预告出来后，我一直很期待。虽然冯导上部《我不是潘金莲》让人略感失望，但他仍是我最喜爱的导演之一。 因为没有合适的同伴，我是一个人去看的。看的...
                                    </div>
                                    <div class="meta">
                                        <nuxt-link to="/c/123" class="collection-tag">社会与法</nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            1500
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            100
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            20
                                        </span>

                                    </div>
                                </div>

                            </li>
                            <li>

                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/p/123" class="avatar">
                                            <img src="~assets/img/default-avatar.jpg">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="'/u/123" class="nickname">测试用户</nuxt-link>
                                            <span class="time">04.12 10:18</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">《芳华》--小萍，愿你被世界温柔以待</nuxt-link>
                                    <div class="abstruct">
                                        我已经很久不去电影院，但是《芳华》预告出来后，我一直很期待。虽然冯导上部《我不是潘金莲》让人略感失望，但他仍是我最喜爱的导演之一。 因为没有合适的同伴，我是一个人去看的。看的...
                                    </div>
                                    <div class="meta">
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            1500
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            100
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            20
                                        </span>

                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <a href="#" class="load-more">阅读更多</a>
                </div>
                <!--占7份，偏移了1份-->
                <div class="col-xs-offset-1 col-xs-7 aside">
                    <div class="row">
                        <!--广告-->
                        <div class="board">
                            <nuxt-link to="/">
                                <img src="~/assets/img/ad1.png">
                            </nuxt-link>
                            <nuxt-link to="/">
                                <img src="~/assets/img/ad2.png">
                            </nuxt-link>
                            <nuxt-link to="/">
                                <img src="~/assets/img/ad3.png">
                            </nuxt-link>
                            <nuxt-link to="/">
                                <img src="~/assets/img/ad4.png">
                            </nuxt-link>
                        </div>
                        <!--推荐作者-->
                        <div class="recommended-author">
                            <div class="title">
                                <span>推荐作者</span>
                                <span @click="whirl">
                                <nuxt-link to="/" class="page-change">
                                    <i class="fa fa-refresh"  ></i>
                                    换一批
                                </nuxt-link>
                                    </span>
                            </div>
                            <ul class="recommended-list">
                                <li>
                                    <nuxt-link class="avatar" to="/u/123">
                                        <img src="~assets/img/default-avatar.jpg">
                                    </nuxt-link>
                                    <a href="#" class="follow" @click="attention">
                                        <i class="fa fa-plus"></i>
                                        关注
                                    </a>
                                    <nuxt-link to="/u/123" class="name">
                                        简书用户
                                    </nuxt-link>
                                    <p>写了1958k字·1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/u/123">
                                        <img src="~assets/img/default-avatar.jpg">
                                    </nuxt-link>
                                    <a href="#" class="follow">
                                        <i class="fa fa-plus"></i>
                                        关注
                                    </a>
                                    <nuxt-link to="/u/123" class="name">
                                        简书用户
                                    </nuxt-link>
                                    <p>写了1958k字·1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/u/123">
                                        <img src="~assets/img/default-avatar.jpg">
                                    </nuxt-link>
                                    <a href="#" class="follow">
                                        <i class="fa fa-plus"></i>
                                        关注
                                    </a>
                                    <nuxt-link to="/u/123" class="name">
                                        简书用户
                                    </nuxt-link>
                                    <p>写了1958k字·1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/u/123">
                                        <img src="~assets/img/default-avatar.jpg">
                                    </nuxt-link>
                                    <a href="#" class="follow">
                                        <i class="fa fa-plus"></i>
                                        关注
                                    </a>
                                    <nuxt-link to="/u/123" class="name">
                                        简书用户
                                    </nuxt-link>
                                    <p>写了1958k字·1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/u/123">
                                        <img src="~assets/img/default-avatar.jpg">
                                    </nuxt-link>
                                    <a href="#" class="follow">
                                        <i class="fa fa-plus"></i>
                                        关注
                                    </a>
                                    <nuxt-link to="/u/123" class="name">
                                        简书用户
                                    </nuxt-link>
                                    <p>写了1958k字·1.9k喜欢</p>
                                </li>
                            </ul>
                            <nuxt-link to="/" class="find-more">
                                查看更多
                                <i class="fa fa-angle-right"></i>
                            </nuxt-link>
                        </div>

                    </div>
                </div>
            </div>
        </div>


    </div>
</template>

<script>
    import myHeader from '../components/myHeader'
    export default {
        head:{
            title:'简书-创作你的创作',
            meta:[
                {charset:'utf-8'},
                {name:'keywords',content:'简书首页'},
                {name:'description',content:'简书首页'},
                {name:'author',content:'MS xu'}
            ]
        },
        components:{
            myHeader
        },
        data() {
            return{
                name:'首页',
                flag:0

            }
        },
        methods:{
            whirl() {
                var whirl=document.querySelector('.index .aside .recommended-author .title .page-change i');
                whirl.style.transform='rotate(720deg)';
                whirl.style.transition='all 1s';
            },

            attention() {
                var whole=document.querySelector('.index .aside .recommended-author .recommended-list li .follow');
                // var check=document.querySelector('.index .aside .recommended-author .recommended-list li .follow i');

                if(this.flag==0){
                    whole.innerHTML='<i class="fa fa-check"></i>'+'已关注';

                    whole.style.color='#969696';
                    this.flag=1;
                    // whole.style.hover=(
                    //     whole.innerHTML='<i class="fa fa-remove"></i>'+'取消关注';
                    // )
                }
                else{
                    whole.innerHTML='<i class="fa fa-plus"></i>'+'关注';
                    whole.style.color='#42c02e';
                    this.flag=0;

                }

            }



        }
    }
</script>
