<template>
<el-container> 
	<el-aside width="200px">        
	 <el-menu
	  default-active="2"
	  class="el-menu-vertical-demo" 
	  default-openeds="1"
	  @open="handleOpen"
	  @close="handleClose">
	  <el-submenu index="1">
	    <template slot="title">
	      <i class="el-icon-location"></i>
	      <span>短信发送</span>
	    </template>
	    <el-menu-item-group>
	      <el-menu-item index="1-1">指定号码群发</el-menu-item>
	      <el-menu-item index="1-2">会员群发短信</el-menu-item>
	    </el-menu-item-group>
	  </el-submenu>
	</el-menu>
	</el-aside>
	<el-main>
	  454545
	</el-main>
</el-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      visible: false,
      msg: 'Welcome to Your Vue.js App',
      defaultOpeneds:[1]
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
