<template>
  <el-menu
    background-color="white"
    active-text-color="red"
    text-color="#222"
    style="min-width: 1300px"
    router
    mode="horizontal"
    :default-active="defaultIndex"
  >
    <el-menu-item
      v-for="(item, index) in navList"
      :index="item.name"
      :key="index"
    >
      {{ item.navItem }}
    </el-menu-item>
    <a href="#nowhere" style="color: #222;float: right;padding: 20px;"
      >更多功能</a
    >
    <i
      class="el-icon-menu"
      style="float:right;font-size: 45px;color: #222;padding-top: 8px"
    ></i>
    <span
      style="position: absolute;padding-top: 20px;right: 43%;font-size: 20px;font-weight: bold"
      >White Jotter - Your Mind Palace</span
    >
  </el-menu>
</template>

<script>
export default {
  name: "NavMenu",
  data() {
    return {
      navList: [
        { name: "/index", navItem: "首页" },
        { name: "/jotter", navItem: "笔记本" },
        { name: "/library", navItem: "图书馆" },
        { name: "/admin", navItem: "个人中心" },
      ],
      defaultIndex:"/index"
    };
  },
};
</script>

<style scoped>
  a{
    text-decoration: none;
  }

  span {
    pointer-events: none;
  }
</style>