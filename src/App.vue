<template>
  <div id="app">
    <treeList :data="list" />
  </div>
</template>

<script>
import treeList from './components/treeList.vue'

export default {
  name: "app",
  components: {
    treeList
  },
  data(){
    return {
      list: [
        {
          label: "一级菜单1",
          children: [
            {
              label: "二级菜单1",
              children: [
                {
                  label: "三级菜单1"
                }
              ]
            },
            {
              label: "二级菜单2"
            }
          ]
        },
        {
          label: "一级菜单2"
        },
        {
          label: "一级菜单3",
          children: [
            {
              label: "二级菜单1"
            }
          ]
        }
      ]
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
