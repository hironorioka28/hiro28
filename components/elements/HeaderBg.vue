<template lang="html">
  <div class="headerBg">
    <div
      :style="bgStyle"
      class="headerBg_bg"
    />
    <div class="headerBg_mask" />
  </div>
</template>

<script>
export default {
  props: {
    imgFile: {
      type: String,
      default: 'IMG_2482.jpg'
    }
  },
  data() {
    const imgPath = require('@/assets/img/' + this.imgFile)
    return {
      bgStyle: {
        backgroundImage: `url(${imgPath})`
      }
    }
  }
}
</script>


<style lang="scss" scoped>
.headerBg {
  width: 100%;
  height: 100%;
  position: relative;
  &_bg,
  &_mask {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: {
      repeat: no-repeat;
      size: cover;
    }
  }
  &_bg {
    background: {
      position: center center;
    }
    filter: brightness(40%);
  }
  &_mask {
    background: {
      image: url('~assets/img/topHeaderMask.svg');
      position: 70% top;
    }
  }
}
</style>
