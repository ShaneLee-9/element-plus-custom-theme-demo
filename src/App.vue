<script setup>
import { onMounted } from "vue";

onMounted(() => {
  console.log('123');
  // document.documentElement is global
const el = document.documentElement
// const el = document.getElementById('xxx')

// get css var
getComputedStyle(el).getPropertyValue(`--el-color-primary`)

// set css var
el.style['--el-color-primary'] = 'red'
})
</script>

<template>
  <el-button type="primary">test</el-button>
  <span class="test-text">test</span>
</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<style lang="scss">
// .test-text {
//   color: $primary;
// }
</style>
