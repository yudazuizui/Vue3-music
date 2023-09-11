<template>
  <div class="topNav">
    <div class="topleft">
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-31liebiao"></use>
      </svg>
    </div>

    <div class="topContent">
      <span
        v-for="(item, index) in musiclists"
        @click="change(index)"
        :key="index"
        :class="isShow === index ? 'active' : ''"
        >{{ item }}</span
      >
    </div>
    <div class="topRight">
      <svg class="icon" aria-hidden="true" @click="$router.push('/search')">
        <use xlink:href="#icon-sousuo"></use>
      </svg>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      musiclists: ['义务', '理塘'],
      isShow: 0
    }
  },
  methods: {
    change (index) {
      this.isShow = index
    }
  }
}
</script>
<style lang="less" scoped>
.topNav {
  width: 100%;
  height: 1rem;
  padding: 0.2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .topContent {
    width: 65%;
    height: 100%;
    display: flex;
    justify-content: space-around;
    // align-items: center;
    font-size: 0.36rem;
    .active {
      font-weight: 900;
    }
  }
}
</style>