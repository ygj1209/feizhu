<template>
  <div class="tab">
    <span
      v-for="(item,index) in ['新闻','体育','军事']"
      :key="index"
      @click="chenag(index)"
      :class="{red:cuorrent===index}"
    >{{item}}</span>

    <div>
      <ul v-if="cuorrent===0">
        <li>新闻豆豆</li>
        <li>打豆豆</li>
        <li>打豆豆</li>
      </ul>
    </div>
    <div>
      <ul v-if="cuorrent===1">
        <li>体育豆豆2</li>
        <li>打豆豆2</li>
        <li>打豆豆2</li>
      </ul>
    </div>
    <div>
      <ul v-if="cuorrent===2">
        <li>军事豆豆3</li>
        <li>打豆豆3</li>
        <li>打豆豆3</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cuorrent: 0
    };
  },
  methods: {
    chenag(index) {
      this.cuorrent = index;
    }
  }
};
</script>

<style lang="less" scoped>
.tab {
  margin-left: 10px;
}
.tab span {
  margin-bottom: 50px;
  padding-left: 20px;
}
.red {
  color: aqua;
}
</style>
