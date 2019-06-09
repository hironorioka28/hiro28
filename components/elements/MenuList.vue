<template lang="html">
  <ul class="menuList">
    <li
      v-for="menu in menuList"
      :key="menu.name"
      :class="{ '_footer': menuType === 'footer' }"
      class="menuList_item"
    >
      <nuxt-link
        :class="{ '_footer': menuType === 'footer' }"
        :to="menu.to"
        class="menuList_link"
      >
        {{ menu.name }}
      </nuxt-link>
    </li>
    <li
      :class="{ '_footer': menuType === 'footer' }"
      class="menuList_item"
    >
      <a
        :class="{ '_footer': menuType === 'footer' }"
        class="menuList_link"
        href="#"
      >
        ABOUT
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    menuType: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      menuList: [
        {
          name: 'BLOG',
          to: '/'
        },
        {
          name: 'WORKS',
          to: '/'
        },
        {
          name: 'PHOTOS',
          to: '/'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.menuList {
  padding: 4px 0;
  @include mq() {
    padding: 0;
  }
  &_item {
    line-height: 1.5;
    &:not(:last-child) {
      margin-bottom: 16px;
    }
    &._footer {
      &:not(:last-child) {
        margin-bottom: 12px;
      }
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
    &._footer {
      font: {
        size: 1.4rem;
      }
    }
  }
}
</style>
