<template lang="html">
  <div class="headerBg">
    <svg
      class="headerBg_mask"
      width="1764.19"
      height="566.164"
      viewBox="0 0 1764.19 566.164"
    >
      <defs>
        <mask
          id="headerBgMask"
        >
          <path id="パス_14" data-name="パス 14" d="M0,0S1450.58-.579,1448.948,0,1122.67,564.116,431.565,565.9-315.241,0-315.241,0Z" transform="translate(315.241 0.257)" fill="rgba(255, 255, 255, 1)" />
        </mask>
      </defs>
    </svg>
    <svg
      class="headerBg_element"
      width="1764.19"
      height="566.164"
      viewBox="0 0 1764.19 566.164"
      preserveAspectRatio="xMidYMid slice"
    >
      <image
        :xlink:href="'_nuxt/assets/img/' + imgUrl"
        class="headerBg_img"
        width="100%"
        height="100%"
        preserveAspectRatio="xMidYMid slice"
      />
    </svg>
  </div>
</template>

<script>
export default {
  props: {
    imgUrl: {
      type: String,
      default: 'IMG_2482.jpg'
    },
    value: {
      type: Number,
      default: 100
    }
  }
}
</script>

<style lang="scss" scoped>
.headerBg {
  filter: brightness(40%);
  &_mask {
    width: 0;
    height: 0;
    position: absolute;
  }
  &_img {
    mask: url(#headerBgMask);
  }
}
</style>
