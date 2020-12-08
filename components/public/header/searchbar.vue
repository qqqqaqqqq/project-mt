<template>
    <div class="search-panel">
        <el-row class="m-header-searchbar">
            <el-col
            :span="3"
            class="left">
                <img src="//s0.meituan.net/bs/fe-web-meituan/fa5f0f0/img/logo.png" alt="美团">              </el-col>
            <el-col
            :span="15"
            class="center">
                <div class="wrapper">
                    <el-input 
                    @focus ="focus"
                    @blur = "blur"
                    v-model="search" 
                    aria-placeholder="搜索商家"></el-input>
                    <button class="el-button el-button--primary">
                        <i class="el-icon-search"></i>
                    </button>
                    <dl v-if="isHotPlace"
                    class="hotPlace">
                        <dt>热门搜索</dt>
                        <dd>火锅</dd>
                        <dd>火锅</dd>
                        <dd>火锅</dd>
                        <dd>火锅</dd>
                    </dl>
                    <dl v-if="isSearchList" 
                    class="searchList">
                        <dd>烧烤</dd>
                        <dd>烧烤</dd>
                        <dd>烧烤</dd>
                    </dl>
                        
                </div>
                    <p class="suggest">
                        <a href="#">故宫博物院</a>
                        <a href="#">故宫博物院</a>
                        <a href="#">故宫博物院</a>
                        <a href="#">故宫博物院</a>   
                    </p>
                    <ul class="nav">
                        <li>
                            <nuxt-link class="takeout" to="/">
                                美团外卖
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link class="hotel" to="/">
                                美团酒店
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link class="movie" to="/">
                                美团电影
                            </nuxt-link>
                        </li>                        
                        <li>
                            <nuxt-link class="apartment" to="/">
                                美团公寓
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link class="business" to="/">
                                商家入驻
                            </nuxt-link>
                        </li>                                                

                    </ul>

                
            </el-col>
            <el-col
            :span="6"
            class="right">
            <ul class="security">
                <li><i class="refund"></i> 不满意</li>
                <li><i class="single"></i>随时退</li>
                <li><i class="overdue"></i>秒到账</li>
            </ul>
            </el-col>
        </el-row>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                search:'',
                isFocus:false,
            }
        },
        methods:{
            focus(){
                this.isFocus = true
            },
            blur(){
                let self = this
                setTimeout(function(){
                    self.isFocus = false
                },200)
            }
        },
        computed:{
            isHotPlace(){
                return this.isFocus&&!this.search
            },
            isSearchList(){
                return this.isFocus&&this.search
            }
        }
        
    }
</script>

<style lang="scss" >

</style>