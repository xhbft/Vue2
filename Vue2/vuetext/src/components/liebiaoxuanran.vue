<template>
  <div class="liebiaoxuanran">
    <hr>
    <h3>列表渲染</h3>
    <div v-for="name in names">{{ name }}</div>
    <div v-for="(name, index) in names">{{ name }}---------{{ index }}</div>
    <div v-for="value in results">
      <p>{{ value.name }}</p >
      <img :src="value.img" alt="value.title">
    </div>
    <div v-for="(value, key, index) in myObject">{{ value }}-----{{ key }}-----{{ index }}</div>
    <hr>
  </div>
</template>

<script>
export default {
  data() {
    return {
      names: ["张三零", "小王", "小李"],
      results: [
        {
          "gkey": "102094068",
          "cmsint1": "0",
          "gde64": "-1",
          "gtype": "双人游戏大全",
          "url": "http://360game.360.cn/flash/102094068.html",
          "gdata": "{\"type\":\"flashgame\",\"appid\":\"102094068\"}",
          "name": "双人游戏大全",
          "img": "//p0.qing.com/com/appstorage/74fcb1bda92f4b050a4009934afa08.png"
        },
        {
          "gkey": "102144745",
          "cmsint1": "0",
          "gde64": "-1",
          "gtype": "餐厅游戏大全",
          "url": "http://360game.360.cn/flash/102144745.html",
          "gdata": "{\"type\":\"flashgame\",\"appid\":\"102144745\"}",
          "name": "餐厅游戏大全",
          "img": "//p2.qing.com/c016c4a2f1a71a8def57.png"
        },
        {
          "gkey": "102146462",
          "cmsint1": "0",
          "gde64": "-1",
          "gtype": "火柴人游戏合集",
          "url": "http://360game.360.cn/flash/102146462.html",
          "gdata": "{\"type\":\"flashgame\",\"appid\":\"102146462\"}",
          "name": "火柴人游戏合集",
          "img": "//p1.qing.com/c014f7e0cc029efefe8a7.png"
        }
      ],
      myObject: {
        title: "游戏列表",
        author: "ADAD",
        Date: "2021-09-01"
      }
    }
  }
}
</script>

<style scoped>
.liebiaoxuanran {
  color: burlywood;
}
</style>