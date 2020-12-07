<template>

<el-row class="m-header"
:gutter="0">
  <el-col :span="4"><div >
      <geo></geo>
      </div></el-col>
  <el-col :span="4"><div>
      <User></User>
      </div></el-col>
  <el-col :span="14"><div class="grid-content bg-purple">
      <Navbar></Navbar>
      </div></el-col>
        
</el-row>


</template>

<script>
import Geo from './geo.vue'
import User from './user.vue'
import Navbar from './nav.vue'
    export default {
        components:{
            Geo,
            User,
            Navbar
        }
    }
</script>

<style lang="scss" >
@import "@/assets/css/public/layout.scss";
@import "@/assets/css/public/header/index.scss";
</style>