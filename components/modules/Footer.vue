<template lang="html">
  <footer class="footer">
    <div class="footer_logo">
      <Logo />
    </div>
    <div class="footer_menu">
      <MenuList
        menu-type="footer"
      />
    </div>
    <div class="footer_sns">
      <SnsList />
    </div>
    <p class="footer_copy">
      &copy; hiro28
    </p>
  </footer>
</template>

<script>
import Logo from '@/components/elements/Logo'
import MenuList from '@/components/elements/MenuList'
import SnsList from '@/components/elements/SnsList'

export default {
  components: {
    Logo,
    MenuList,
    SnsList
  }
}
</script>

<style lang="scss" scoped>
.footer {
  padding: 72px 32px 32px 32px;
  position: relative;
  overflow: hidden;
  @include mq(1000) {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  &::after {
    background-color: $black-m;
    border-radius: 0 150vw 0 0 / 0 470px 0 0;
    display: block;
    content: '';
    position: absolute;
    top: 0;
    right: -50vw;
    bottom: 0;
    left: 0;
    z-index: -1;
  }
  &_menu,
  &_sns,
  &_copy {
    @include mq(1000) {
      width: 1000px - 64px;
    }
  }
  &_logo {
    margin-bottom: 40px;
    width: 86px;
    @include mq(1000) {
      margin-right: 1000px - 64px - 86px;
    }
  }
  &_menu {
    margin-bottom: 40px;
  }
  &_sns {
    margin-bottom: 80px;
  }
  &_copy {
    color: $white-l;
    font: {
      weight: 200;
    }
  }
}
</style>
