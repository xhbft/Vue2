<template>
  <div class="new-container" v-if="showContent">
    <h1>NEW新组建集合11.13</h1>
    <nav class="navigation">
      <router-link to="/" class="nav-link">返回首页</router-link>
    </nav>
    <hr>
    <zuhexiangyingshi></zuhexiangyingshi>
    <zuhejisuanshuxing></zuhejisuanshuxing>
  </div>
</template>

<script>
import zuhexiangyingshi from "../newcomponents/zuhexiangyingshi.vue";
import zuhejisuanshuxing from "../newcomponents/zuhejisuanshuxing.vue";

export default {
  name: "new",
  data() {
    return {
      showContent: false,
    };
  },
  components: {
    zuhexiangyingshi,
    zuhejisuanshuxing
  },
  mounted() {
    setTimeout(() => {
      this.showContent = true;
    }, 0);
  }
}
</script>

<style scoped>
.new-container {
  position: relative;
  z-index: 10;
}

h1 {
  z-index: 11;
  color: aqua;
}

.navigation {
  margin: 20px 0;
  z-index: 11;
}
</style>