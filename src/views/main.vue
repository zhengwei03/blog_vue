<template>
  <el-container class="container_in">
    <el-container>
      <el-aside class="aside_in" width="200px">Aside</el-aside>
      <el-container>
        <el-main class="main_in">
          <el-row>
            <el-col :span="24">
              <!-- <div class="grid-content ep-bg-purple-dark"><el-image style="width: 100px; height: 100px" :src="@/assets/a.jpg" :fit="fit" /></div> -->
            </el-col>
          </el-row>
        </el-main>
      </el-container>
    </el-container>
    <el-aside class="aside_in" width="200px">Aside</el-aside>
  </el-container>
</template>


<script>
export default {
  name: "app",
  components: {},
};
</script>

<style scoped>
.container_in {
  position: relative;
  padding: 0;
  width: 100%;
  height: 100%;
}

.aside_in .main_in {
  position: absolute;
  top: 0;
  left: 0;
  padding: 2px 0;
  width: 100%;
  height: 100%;
  opacity: 0.5;

  /* border: 0px 1px 1px 1px solid #e2e1e1; */
}

.el-header {
  background-color: #ffffff;
  color: #333;
  text-align: center;
}

.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  border-bottom: 1px solid #e2e1e1;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.el-aside {
  background-color: #ffffff;
  color: #333;
  text-align: center;
  margin: 2px;
  width: 18%;
  border: #e2e1e1;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.el-main {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 2px;
  background-color: #ffffff;
  color: #333;
  text-align: center;
  border-bottom: 1px solid #e2e1e1;
  box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.1);
  padding: 5px 0;
}

.el-row {
  margin-bottom: 20px;
}

.el-row:last-child {
  margin-bottom: 0;
}

.el-col {
  border-radius: 4px;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

.grid-content{
  background-color: aqua;
}
</style>
