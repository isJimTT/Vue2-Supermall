<template>
  <swiper class="detail-swiper">
    <swiper-item v-for="(item, index) in detailSwiper" :key="index">
      <img :src="item" alt="">
    </swiper-item>
  </swiper>
</template>

<script>

import {Swiper, SwiperItem} from 'components/common/swiper'

export default {
  name: "detailSwiper",
  components: {
    Swiper,
    SwiperItem
  },
  props: {
    detailSwiper: {
      type: Array,
      default() {
        return []
      }
    }
  }
}
</script>

<style scoped>
  .detail-swiper {
    height: 300px;
    overflow: hidden;
  }
</style>
