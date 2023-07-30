<template>
  <div id="header_menu">
    <el-menu
      :default-active="activeIndex2"
      class="el-menu-demo"
      mode="horizontal"
      background-color="#FFFFFF"
      text-color="#000000"
      active-text-color="#409EFF"
      router
      @select="handleSelect"
    >
      <div class="logo-container">
        <img class="logo_img" src="@/assets/blog_logo.png" alt="Logo" />
      </div>
      <el-menu-item index="1">首页</el-menu-item>
      <el-sub-menu index="2">
        <template #title>分类</template>
        <el-menu-item index="2-1">Python</el-menu-item>
        <el-menu-item index="2-2">Django</el-menu-item>
        <el-menu-item index="2-3">Vue</el-menu-item>
        <!-- <el-sub-menu index="2-4">
          <template #title>item four</template>
          <el-menu-item index="2-4-1">item one</el-menu-item>
          <el-menu-item index="2-4-2">item two</el-menu-item>
          <el-menu-item index="2-4-3">item three</el-menu-item>
        </el-sub-menu> -->
      </el-sub-menu>
      <el-menu-item index="3">博客</el-menu-item>
      <el-menu-item index="4">demo</el-menu-item>
      <!-- <li style="display: flex; align-items: center;justify-content:flex-end">
        <el-input placeholder="Search" style="margin-right: 20px"></el-input>
        <el-button type="text" size="small">Register</el-button>
        <el-button type="primary" size="small">Log In</el-button>
      </li> -->
      <div class="search-box">
        <el-input placeholder="Search..." class="search-input"></el-input>
      </div>
      <div class="user-info">
        <el-button type="text" class="login-btn">Login</el-button>
        <!-- <el-button type="primary" class="register-btn">Register</el-button>
        <el-button type="primary" class="register-btn">Register</el-button>
        <el-button type="primary" class="register-btn">Register</el-button> -->
      </div>
    </el-menu>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const activeIndex = ref("1");
const activeIndex2 = ref("1");
const handleSelect = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
</script>

<style scoped>
#header_menu {
  display: flex;
  align-items: center;
  height: 60px;
  padding: 0;
  justify-content: space-between; /* 让 logo 和 menu 两侧对齐 */
  background-color: #fff;
  border-bottom: 1px solid #e2e1e1;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.el-menu-demo {
  flex-grow: 1;
  display: flex;
  align-items: center;
  border-bottom: 1px solid #e2e1e1;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.search-container {
  margin-left: auto;
  margin-right: auto;
}

.logo_img {
  width: 40px;
  height: auto;
  position: relative;
  border-radius: 30px;
  margin: 0 20px;
}

.el-menu-item {
  /* color: #fff; */
  position: relative;
  background: rgba(255, 252, 252, 0.3);
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
  padding: 0 30px;
}

.search-box {
  /* flex: 1; 让 .search-box 占据剩余空间 */
  display: flex;
  justify-content: center;
  align-items: center;
    width: 300px;
}

.search-input {
  width: 400px;
  margin: 0 50px;
}

.user-info {
  display: flex;
  align-items: center;
  margin-left: auto; /* 把 .user-info 推到最右侧 */
  position: relative;
  right: 2%;
}
</style>


