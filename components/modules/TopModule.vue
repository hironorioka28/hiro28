<template lang="html">
  <section class="topModule">
    <h2 class="topModule_title">
      <span
        :v-if="titleModifier !== ''"
        class="topModule_titleModifier"
      >
        {{ titleModifier }}
      </span>
      {{ title }}
    </h2>
    <div class="topModule_body">
      <slot name="topModuleBody" />
    </div>
    <footer
      v-if="linkToMore !== ''"
      class="topModule_footer"
    >
      <nuxt-link
        :to="linkToMore"
        class="topModule_more"
      >
        MORE
      </nuxt-link>
    </footer>
  </section>
</template>

<script>
export default {
  props: {
    titleModifier: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: 'TOPMODULE'
    },
    linkToMore: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.topModule {
  padding-top: 40px;
  position: relative;
  &_title {
    position: absolute;
    top: 0;
    left: -36px;
    font: {
      size: 6rem;
      weight: 900;
    }
    color: rgba($gray-l, 0.6);
    line-height: 1;
    z-index: -1;
  }
  &_titleModifier {
    display: block;
    position: absolute;
    top: -10px;
    left: 5px;
    font: {
      size: 1.5rem;
      weight: 400;
    }
    color: $gray-l;
  }
  &_footer {
    margin-top: 40px;
  }
  &_more {
    display: block;
    text-align: center;
    font: {
      size: 2rem;
      weight: 400;
    }
    letter-spacing: 0.4em;
    &::after {
      content: '\f105';
      font: {
        family: 'Font Awesome 5 Free';
        weight: 900;
      }
    }
  }
}
</style>
