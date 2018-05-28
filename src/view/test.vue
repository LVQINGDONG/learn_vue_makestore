<template>
<div class="test">
this is id :{{$route.params.testId}}
<br/>
<router-link to="/test/title1">标题1</router-link>
<router-link to="/test/title2">标题2</router-link>
<router-view></router-view>
<div @click="gotoGoods">点击跳转到商品详情页面</div>
</div>
</template>
<script>
export default{
    data(){
        return{
            msg:'hello vue'
        }
    },
    methods:{
        gotoGoods(){
            this.$router.push('/goods');
        }
    }
}
</script>
<style scoped>
</style>
