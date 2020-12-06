<template>

<el-row 
class="m-header"
:gutter="15">
  <el-col :span="6"><div class="grid-content bg-purple">
      <geo></geo>
      </div></el-col>
  <el-col :span="6"><div class="grid-content bg-purple">
      <User></User>
      </div></el-col>
  <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
  
</el-row>


</template>

<script>
import Geo from './geo.vue'
import User from './user.vue'
    export default {
        components:{
            Geo,
            User
        }
    }
</script>

<style lang="scss" scoped>
@import "@/assets/css/public/layout.scss" 

</style>