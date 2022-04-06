<template>
  <div>
    {{isShow}}
  </div>
</template>

<script>
import bus from "../bus.js";

export default {
  name: 'TestPage',
  data() {
    return {
      isShow: false
    }
  },
  mounted(){
    bus.$on("isShow", (val) => {
      this.isShow = val;
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
