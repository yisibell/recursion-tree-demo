<template>
  <p>
    <span @click="toggle">{{folder.label}}</span>
    <treeList v-show="isshow" :data="folder.children"></treeList>
  </p>
</template>


<script>
// 异步导入 treeList 组件，告诉模块系统 -> 我们不需要先解析 treeList 组件，等到用到的时候再解析加载
const treeList = () => import('./treeList.vue')

export default {
  name: "treeLabel",
  data(){
    return {
      isshow: false
    }
  },
  props: ['folder'],
  components: {
    treeList
  },
  methods: {
    toggle(){
      this.isshow = !this.isshow;
    }
  }
}
</script>

<style scoped>
 span { cursor: pointer;}
</style>

