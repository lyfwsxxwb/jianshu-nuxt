<template>
    <div>
        <my-header></my-header>
        <p>我的主体部分</p>
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
                name:'首页'
            }
        }
    }
</script>

<style>

</style>