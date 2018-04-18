<template>
    <div>注册</div>
</template>

<script>
    export default {
        //修改当前页面的默认模板为sign.vue
        //如果不写的话，默认是default.vue
        layout:'sign',
        //设置页面的标题以及描述、关键字等元信息
        head: {
            title: '注册-简书',
            meta: [
                {charset:'utf-8'},
                {name: 'keywords', content: '注册页面'},
                {name: 'description', content: '注册简书'},
                {name: 'author', content: 'MS xu'}
            ]
        },
        data() {
            return {}
        }
    }
</script>
<style scoped>

</style>

