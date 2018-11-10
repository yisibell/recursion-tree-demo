<template>
  <p>
    <span @click="toggle">{{folder.label}}</span>
    <treeList v-show="isshow" :data="folder.children"></treeList>
  </p>
</template>


<script>
var treeList = () => import('./treeList.vue')

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

