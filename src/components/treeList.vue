<template>
  <ul>
    <li v-for="(child,index) in data" :key="index">
      <treeLabel v-if="child.children" :folder="child"></treeLabel>
      <span v-else>{{child.label}}</span>
    </li>
  </ul>
</template>

<script>

import treeLabel from './treeLabel.vue'

export default {
  name: "treeList",
  components: {
    treeLabel
  },
  props: ['data']
}
</script>


<style scoped>
  ul { list-style: none;}
  p { margin: 0}
</style>



