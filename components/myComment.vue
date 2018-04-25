<template>
    <div class="comment-list">
        <!--提交新内容的表单-->
        <my-form>
            <nuxt-link to="/u/123" class="avatar">
                <img src="~/assets/img/default-avatar.jpg">
            </nuxt-link>
        </my-form>
        <div class="normal-comment-list">
            <!--显示留言的信息-->
            <div class="top-title">
                <span>1条评论</span>
                <a href="#" class="author-only">只看作者</a>
                <div class="pull-right">
                    <a href="#" class="active">按喜欢排序</a>
                    <a href="#">按时间正序</a>
                    <a href="#">按时间倒序</a>
                </div>
            </div>
            <!--显示所有留言的内容-->
            <div class="comment">
                <div class="author">
                    <div class="v-tooltip-container">
                        <nuxt-link to="/u/123" class="avatar">
                            <img src="~/assets/img/default-avatar.jpg"
                        </nuxt-link>
                    </div>
                    <div class="info">
                        <nuxt-link to="/u/123" class="name">
                            简书注册用户
                        </nuxt-link>
                        <div class="meta">
                            <span>2楼 · 2018.03.15 09:52</span>
                        </div>
                    </div>
                </div>
                <div class="comment-wrap">
                    <p>加油</p>
                    <div class="tool-group">
                        <a href="#" class="zan">
                            29人赞
                        </a>
                        <a href="#" class="comment-btn">
                            <i class="fa fa-comment-o"></i>
                            <span>回复</span>
                        </a>
                    </div>
                </div>
                <div class="sub-comment-list"></div>
            </div>
        </div>
    </div>
</template>

<script>
    import myForm from '~/components/myForm'
    export default {
        name: "myComment",
        components:{
            myForm
        },
        data(){
            return{
                comments:[
                    {
                        id:19935725,
                        floor:2,
                        liked:true,
                        likes_count:20,
                        note_id:23054702,
                        user_id:6780849,
                        user:{
                            avatar:'/default-avatar.jpg',
                            id:6780849,
                            is_author:false,
                            nick_name:'七岁就很拽',
                            badge:null,

                        },
                        create_at:'2018-01-25T09:38:14.000+08:00',
                        children_count:4,
                        compiled_content:'今年25岁的我，年纪轻轻月薪就已经达到2800了，加上提成满勤再加上我天生的睿智头脑，平常帮客人拿下拖鞋点下烟得点小费可以拿到3100。觉得自己这几年过得也不容易，现在这么有钱，都不知道怎么花了，开始花钱大手大脚了，以前网吧包夜都是喝自来水，现在敢喝红茶了，还是一晚上买两瓶，甚至打电话出去叫炒河粉而且还要加个鸡蛋，我觉得现在有点迷失自我，有什么办法？希望能回到初心！',
                        children:[
                            {
                                id:20116365,
                                user_id:2604707,
                                user:{
                                    id:2604707,
                                    nick_name:'Bowman_'
                                },
                                parent_id:19935725,                                         create_at:'2018-01-30T11:23:03.000+08:00',
                                compiled_content:'兄die,我也和你有着一样的困惑，甚至一度迷失自我...'
                            },
                            {
                                id:20122216,
                                user_id:9933465,
                                user:{
                                    id:9933465,
                                    nick_name:'美女荷官'
                                },
                                parent_id:19935725,                                         create_at:'2018-01-30T14:25:32.000+08:00',
                                compiled_content:'是你李大钊飘了,还是我陈独秀拿不动刀了'
                            },
                            {
                                id:20122226,
                                user_id:9964877,
                                user:{
                                    id:9964877,
                                    nick_name:'保坤文化传媒'
                                },
                                parent_id:19935725,                                         create_at:'2018-01-30T14:25:49.000+08:00',
                                compiled_content:'哈哈。。'
                            },
                        ]
                    },
                    {
                        id:19935796,
                        floor:3,
                        liked:false,
                        likes_count:30,
                        create_at: "2018-01-25T09:40:18.000+08:00",
                        note_id:23054702,
                        user_id:6780849,
                        user:{
                            avatar:'/default-avatar.jpg',
                            id:6780849,
                            is_author:false,
                            nick_name:'七岁就很拽',
                            badge:null,

                        },
                        compiled_content:'作为一名混凝土方块移动工程师，我一直以3000的月薪骄傲，甚至一度迷失自我。。。看了楼主这篇文章，我找回了初心',
                        children_count:3,
                        children:[
                            {
                                id:19949215,
                                parent_id:19935796,
                                user_id:5954136,
                                user:{
                                    id:5954136,
                                    nick_name:'与笑颜开'
                                },
                                create_at:'2018-01-25T16:55:40.000+08:00',
                                compiled_content:'混凝土方块移动工程师是啥子工作，我咋没听过？我也做过混凝土这行'
                            },
                            {
                                id:20062029,
                                parent_id:19935796,
                                user_id:8914781,
                                user:{
                                    id:8914781,
                                    nick_name:'向天再借5厘米'
                                },
                                create_at:'2018-01-28T21:06:14.000+08:00',
                                compiled_content:'<a href="/users/88ad9c9678a6" class="maleskine-author" target="_blank" data-user-slug="88ad9c9678a6">@与笑颜开</a> 搬砖'
                            },
                            {
                                id:20122231,
                                parent_id:19935796,
                                user_id:9964877,
                                user:{
                                    id:9964877,
                                    nick_name:'保坤文化传媒'
                                },
                                create_at:'2018-01-25T16:55:40.000+08:00',
                                compiled_content:'好有意思。'
                            },
                        ]
                    },
                    {
                        children: [],
                        children_count:0,
                        compiled_content: "楼上评论的都是大佬啊",
                        create_at: "2018-01-29T11:26:53.000+08:00",
                        floor:4,
                        id:20080144,
                        liked:false,
                        likes_count:2,
                        note_id: 23054702,
                        user:
                            {
                                id: 3160769,
                                nick_name: "yuebiubiu",
                                is_author:false,
                                avatar:'/default-avatar.jpg'
                            },
                        user_id:3160769
                    }
                ],
            }
        }
    }
</script>

<style scoped>
    .comment-list{
        padding-top: 20px;
    }
    /*.comment-list .new-comment{*/
        /*position: relative;*/
        /*margin: 0 0 20px 56px;*/
    /*}*/
    /*.comment-list .new-comment .avatar{*/
        /*width: 38px;*/
        /*height: 38px;*/
        /*position: absolute;*/
        /*left: -38px;*/
        /*display: inline-block;*/
        /*margin-right: 10px;*/
    /*}*/
    /*.comment-list .new-comment textarea{*/
        /*padding: 10px 15px;*/
        /*width: 100%;*/
        /*height: 80px;*/
        /*outline: none;*/
        /*resize: none;*/
        /*display: inline-block;*/
        /*font-size: 13px;*/
        /*border:1px solid #dcdcdc;*/
        /*background: #f7f7f7;*/
        /*border-radius: 4px;*/
        /*vertical-align: top;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block{*/
        /*height: 50px;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block .emoji{*/
        /*float: left;*/
        /*margin-top: 14px;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block .emoji i{*/
        /*font-size: 20px;*/
        /*color:#969696;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block .emoji i:hover{*/
        /*color: #2f2f2f;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block .hint{*/
        /*float: left;*/
        /*margin:18px 0 0 20px;*/
        /*font-size: 13px;*/
        /*color: #969696;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block .btn-send{*/
        /*float: right;*/
        /*width: 78px;*/
        /*padding: 8px 18px;*/
        /*margin: 10px 0;*/
        /*display: block;*/
        /*font-size: 16px;*/
        /*background: #42c02e;*/
        /*color: #fff;*/
        /*text-align: center;*/
        /*border-radius: 20px;*/
        /*outline: none;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block .btn-send:hover{*/
        /*background: #3db922;*/
    /*}*/
    /*.comment-list .new-comment .write-function-block .btn-cancel{*/
        /*float: right;*/
        /*margin: 18px 30px 0 0;*/
        /*font-size: 16px;*/
        /*color: #969696;*/
    /*}*/
    .comment-list .normal-comment-list{
        margin-top:30px ;
    }
    .comment-list .normal-comment-list .top-title{
        padding-bottom: 20px;
        border-bottom:1px solid #e1e1e1;
        font-size: 17px;
        font-weight: 700;
    }
    .comment-list .normal-comment-list  .top-title span{
        vertical-align: middle;
    }
    .comment-list .normal-comment-list  .top-title .author-only{
        margin-left: 10px;
        padding: 4px 8px;
        font-size: 12px;
        color: #969696;
        border:1px solid #dcdcdc;
        border-radius: 20px;
    }
    .comment-list .normal-comment-list  .top-title .pull-right{
        float: right;
    }
    .comment-list .normal-comment-list  .top-title .pull-right a{
        font-size: 12px;
        color:#969696;
        margin-left: 10px;
        font-weight: 400;
    }
    .comment-list .normal-comment-list  .top-title .pull-right a.active{
        color:#2f2f2f;
    }

    /*评论部分*/
    .comment-list .comment{
        padding: 20px0 30px 0;
        border-bottom: 1px solid #f0f0f0;
    }

</style>