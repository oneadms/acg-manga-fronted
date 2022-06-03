<template>
  <div class="row align-items-center border-1"
       style="height: 60px"
  >
    <div
         style="display: inline-block; cursor: pointer;white-space: nowrap;flex-wrap: nowrap;"
    >
      <img src="~/static/logo.png"/>
    </div>
    <div class="col nav-item" >首页</div>
    <div class="col nav-item" >同人漫画</div>
    <div class="col nav-item" >同人图</div>
    <div class="col nav-item" >全彩漫画</div>
    <div class="col nav-item" >合辑</div>
    <div class="col nav-item" >网漫</div>
    <div class="col nav-item" >专题</div>
    <div class="col nav-item" >动漫</div>
    <el-row>
      <el-col :span="18">
        <el-input v-model="searchContent"></el-input>
      </el-col>
      <el-col :span="6" >
        <el-button>搜索</el-button>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      searchContent:''
    }
  }
}
</script>

<style scoped>
.nav-item:hover{
  color: #ff64c5;
  cursor: pointer;
}

</style>
