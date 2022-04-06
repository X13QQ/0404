<template>
  <div id="app">
    <a href="#" class="head-icon" @click.prevent="openCart">
      購物車開
    </a>
    <a href="#" class="head-icon" @click.prevent="closeCart">
      購物車關
    </a>
    <TestPage></TestPage>
  </div>
</template>

<script>
import TestPage from './pages/TestPage.vue'
import bus from "./bus.js";

export default {
  name: 'App',
  components: {
    TestPage
  },
  methods:{
    openCart(){
      bus.$emit("isShow", true);
    },
    closeCart(){
      bus.$emit("isShow", false);
    }
  }
}
</script>

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
