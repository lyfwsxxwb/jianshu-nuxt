<template>
    <div>
        <form class="new-comment" method="post">
            <slot></slot>
            <textarea name="comment-content" placeholder="写下你的评论"></textarea>
            <div class="write-function-block">
                <div class="emoji-modal-wrap">
                    <a href="#" class="emoji">
                        <i class="fa fa-smile-o"></i>
                    </a>
                    <div class="emoji-modal"></div>
                </div>
                <div class="hint">Ctrl+Enter发表</div>
                <a href="#" class="btn-send">发送</a>
                <a href="#" class="btn-cancel">取消</a>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        name: "myForm",
        data(){
            return{

            }
        }
    }
</script>

<style scoped>
    .comment-list .new-comment{
        position: relative;
        margin: 0 0 20px 56px;
    }
    .comment-list .new-comment .avatar{
        width: 38px;
        height: 38px;
        position: absolute;
        left: -38px;
        display: inline-block;
        margin-right: 10px;
    }
    .comment-list .new-comment textarea{
        padding: 10px 15px;
        width: 100%;
        height: 80px;
        outline: none;
        resize: none;
        display: inline-block;
        font-size: 13px;
        border:1px solid #dcdcdc;
        background: #f7f7f7;
        border-radius: 4px;
        vertical-align: top;
    }
    .comment-list .new-comment .write-function-block{
        height: 50px;
    }
    .comment-list .new-comment .write-function-block .emoji{
        float: left;
        margin-top: 14px;
    }
    .comment-list .new-comment .write-function-block .emoji i{
        font-size: 20px;
        color:#969696;
    }
    .comment-list .new-comment .write-function-block .emoji i:hover{
        color: #2f2f2f;
    }
    .comment-list .new-comment .write-function-block .hint{
        float: left;
        margin:18px 0 0 20px;
        font-size: 13px;
        color: #969696;
    }
    .comment-list .new-comment .write-function-block .btn-send{
        float: right;
        width: 78px;
        padding: 8px 18px;
        margin: 10px 0;
        display: block;
        font-size: 16px;
        background: #42c02e;
        color: #fff;
        text-align: center;
        border-radius: 20px;
        outline: none;
    }
    .comment-list .new-comment .write-function-block .btn-send:hover{
        background: #3db922;
    }
    .comment-list .new-comment .write-function-block .btn-cancel{
        float: right;
        margin: 18px 30px 0 0;
        font-size: 16px;
        color: #969696;
    }
</style>