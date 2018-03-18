<template>
  <el-container>
    <el-header>
      <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect"
        background-color="#409EFF"
        text-color="#fff"
        active-text-color="#fff"
      >
        <el-menu-item index="0" disabled>
          <h1>
            <img src="/assets/logo.png">
          </h1>
        </el-menu-item>
        <el-submenu index="1">
          <template slot="title">短信发送</template>          
          <el-menu-item index="1-1">指定号码群发</el-menu-item>  
          <el-menu-item index="1-2">会员群发短信</el-menu-item>      
        </el-submenu>

        <el-menu-item index="2">短信设置</el-menu-item>
        
        <el-menu-item index="3">会员管理</el-menu-item>
      </el-menu>
    </el-header>         
    <router-view/>    
  </el-container>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      activeIndex: '1-1'
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style>
  body,html{
    margin: 0;
    padding: 0;
  }
 .el-header, .el-footer {
    background-color: #409EFF;
    text-align: center;
    line-height: 60px;
  }
  .el-menu--horizontal>.el-menu-item.is-active {
    border-bottom: 0px solid #409EFF;
    background-color: #337ecc !important;
  }
  .el-menu--horizontal>.el-menu-item{
    border-bottom: 0px;
  }
  .el-menu--horizontal>.el-submenu.is-active .el-submenu__title {
    border-bottom: 0px solid #409EFF;
    background-color: #337ecc !important;
  }
  .el-menu--horizontal>.el-submenu .el-submenu__title {
    border-bottom: 0px;
  }
  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    line-height: 200px;
  }
  
  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  
  body > .el-contaiern {
    margin-bottom: 40px;
  }
  
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>
