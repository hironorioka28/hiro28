<template lang="html">
  <header class="topHeader">
    <div class="topHeader_main">
      <div class="topHeader_logo">
        <Logo />
      </div>
      <div class="topHeader_list">
        <HeaderList />
      </div>
    </div>
    <div class="topHeader_today">
      <Today />
    </div>
    <div class="topHeader_bg">
      <HeaderBg
        img-url="IMG_2482.jpg"
      />
    </div>
  </header>
</template>

<script>
import Logo from '@/components/elements/Logo'
import HeaderList from '@/components/elements/HeaderList'
import HeaderBg from '@/components/elements/HeaderBg'
import Today from '@/components/elements/Today'

export default {
  components: {
    Logo,
    HeaderList,
    HeaderBg,
    Today
  }
}
</script>

<style lang="scss" scoped>
.topHeader {
  height: calc(100vh - 32px * 2);
  padding: 32px;
  background-color: $white-l;
  position: relative;
  &_main {
    display: flex;
    align-items: flex-end;
    position: relative;
    z-index: 1;
    mix-blend-mode: exclusion;
    @include mq() {
      display: block;
    }
  }
  &_logo {
    order: 2;
    flex-grow: 1;
    max-width: 240px;
    @include mq() {
      width: 160px;
    }
  }
  &_list {
    margin-right: 40px;
    order: 1;
    flex-shrink: 0;
    @include mq() {
      margin: 40px 0 0 0;
    }
  }
  &_bg {
    position: fixed;
    top: 0;
    right: -100vw;
    @include mq() {
      right: unset;
      left: -20vw;
    }
  }
  &_today {
    position: absolute;
    right: 32px;
    bottom: 32px;
    mix-blend-mode: exclusion;
    z-index: 1;
    color: $white-l;
  }
}
</style>
