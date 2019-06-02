<template lang="html">
  <ul class="headerList">
    <li class="headerList_item">
      <nuxt-link
        to="/"
        class="headerList_link"
      >
        BLOG
      </nuxt-link>
    </li>
    <li class="headerList_item">
      <nuxt-link
        to="/"
        class="headerList_link"
      >
        WORKS
      </nuxt-link>
    </li>
    <li class="headerList_item">
      <nuxt-link
        to="/"
        class="headerList_link"
      >
        PHOTOS
      </nuxt-link>
    </li>
    <li class="headerList_item">
      <a
        href="#"
        class="headerList_link"
      >
        ABOUT
      </a>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
.headerList {
  padding: 4px 0;
  @include mq() {
    padding: 0;
  }
  &_item {
    &:not(:last-child) {
      margin-bottom: 16px;
    }
  }
  &_link {
    color: $white-l;
    font: {
      size: 2rem;
      weight: bold;
    }
    letter-spacing: 0.05em;
    line-height: 1;
    @include mq(375) {
      font: {
        size: 2.4rem;
      }
    }
  }
}
</style>
