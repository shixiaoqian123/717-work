<template>
    <div class="container">
        <router-view class="wrap"></router-view>

        <nav>
            <router-link :to="{name:'home'}" tag="span">
                <em class="icon iconfont icon-home"></em>
                <sub>首页</sub>
            </router-link>

            <router-link :to="{name:'category'}" tag="span">
                <em class="icon iconfont icon-apps"></em>
                <sub>分类</sub>
            </router-link>

            <router-link :to="{name:'cart'}" tag="span">
                <em class="icon iconfont icon-cart"></em>
                <sub>购物车</sub>
            </router-link>

            <router-link :to="{name:'mine'}" tag="span">
                <em class="icon iconfont icon-people"></em>
                <sub>我的</sub>
            </router-link>

        </nav>
       <!--  <div @click="to_community">社区</div> -->
    </div>
</template>
<script>
export default {
    methods:{
        to_community(){
            this.$router.push({name:'community'})
        }
    }
}
</script>
<style>
.container {
    height: 100%;
    display: flex;
    flex-direction: column;
}

.wrap {
    flex: auto;
}

nav {
    height: 0.98rem;
    text-align: center;
    display: table;
    width: 100%;
    border-top: 1px solid #eee;
}

nav span {
    display: table-cell;
    width: 25%;
}

nav .icon {
    font-size: 0.46rem;
}

nav em,
nav sub {
    display: block;
    width: 100%;
}

nav .icon {
    height: 0.5rem;
}
</style>

