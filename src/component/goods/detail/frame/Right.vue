<template>
    <div class="sidebar-box">
        <h4>推荐商品</h4>
        <ul class="side-img-list">

            <li v-for="(item,i) in hotgoodslist" :key="item.id">
                <div class="img-box">
                    <!-- <a href="/goods/show-98.html">
                                <img src="item.img_url">
                            </a>  -->
                    <router-link :to="{ name:'gd' , params:{id:item.id} }">
                        <label>{{i+1}}</label>
                        <img :src="item.img_url">
                    </router-link>
                </div>
                <div class="txt-box">
                    <!-- <a href="/goods/show-98.html">奔腾（BNTN） 380功放+纽约至尊 套装家庭影院</a> -->
                    <router-link :to="{ name:'gd' , params:{id:item.id} }">
                        {{item.title}}
                    </router-link>
                    <span>{{item.add_time | date}}</span>
                </div>
            </li>

        </ul>
    </div>
</template>

<script>
export default {
    props: ['hotgoodslist']
}
</script>

<style scoped>

</style>