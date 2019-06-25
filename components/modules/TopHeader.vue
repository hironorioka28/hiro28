<template lang="html">
  <header class="topHeader">
    <div class="topHeader_bg">
      <HeaderBg />
    </div>
    <div class="topHeader_main">
      <div class="topHeader_logo">
        <Logo />
      </div>
      <div class="topHeader_list">
        <MenuList />
      </div>
    </div>
    <div class="topHeader_today">
      <Today />
    </div>
  </header>
</template>

<script>
import Logo from '@/components/elements/Logo'
import MenuList from '@/components/elements/MenuList'
import HeaderBg from '@/components/elements/HeaderBg'
import Today from '@/components/elements/Today'

export default {
  components: {
    Logo,
    MenuList,
    HeaderBg,
    Today
  }
}
</script>

<style lang="scss" scoped>
.topHeader {
  padding: 32px;
  height: calc(100vh - 32px * 2);
  background-color: $white-l;
  position: relative;
  @include mq() {
    height: calc(500px - 32px * 2);
  }
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
    width: 100vw;
    height: 100vh;
    position: absolute;
    top: 0;
    left: 0;
    @include mq() {
      height: 600px;
    }
    @include mq(1000) {
      left: calc(-1 * (100vw - 1000px) / 2);
    }
  }
  &_today {
    position: absolute;
    right: 32px;
    bottom: 32px;
    mix-blend-mode: exclusion;
    z-index: 1;
    color: $white-l;
    @include mq() {
      bottom: 42px;
    }
  }
}
</style>
