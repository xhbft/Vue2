<template>
  <div class="divdiv" v-if="showContent">
    <h3 class="title">各类组件+++++</h3>
    <nav class="navigation">
      <router-link to="/new" class="nav-link">跳转到new</router-link>
    </nav>
    <hr>
    <Swiper></Swiper>
  </div>
</template>

<script>
import Swiper from '../newnewcomponents/swiper.vue'
export default {
  name: 'geleizujian',
  components: {
    Swiper
  },
  data() {
    return {
      showContent: false,
    }
  },
  mounted() {
    setTimeout(() => {
      this.showContent = true;
    }, 0);
  }
}
</script>

<style scoped>
.divdiv {
  position: relative;
  z-index: 10;
}

.title {
  color: red;
  margin-bottom: 20px;
}

.navigation {
  margin: 20px 0;
  z-index: 11;
}
</style>