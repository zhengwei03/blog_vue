<template>
  <div class="container_app">
    <el-container class="container_app">
      <el-header class="header_app"><Header></Header></el-header>
      <el-main class="main_app">
        <Main></Main>
      </el-main>
      <el-footer class="footer_app">Footer</el-footer>
    </el-container>
  </div>
</template>


<script>
import Header from "@/components/header.vue";
import Main from "@/views/main.vue";

export default {
  name: "app",
  components: {
    Header,
    Main,
  },
};
</script>


<style scoped>
.container_app {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* background-image: ; */
}

.header_app {
  padding: 0 18%;
  height: 60px;
}

.footer_app {
  margin: 0 18%;
  height: 60px;
  border-bottom: 1px solid #e2e1e1;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.main_app {
  margin: 0;
  padding: 0 18%;
  width: 100%;
  height: 100%;
}

.el-footer {
  background-color: #ffffff;
  color: #333;
  text-align: center;
}

.el-aside {
  background-color: #ffffff;
  color: #333;
  text-align: center;
}

.el-main {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #333;
  text-align: center;
}

body > .el-container {
  margin-bottom: 40px;
  width: 100vh;
  height: 100vh;
}
</style>
