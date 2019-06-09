<template>
  <section class="page_wrapper">
    <section class="page_header">
      <TopHeader />
    </section>
    <section class="page_section">
      <TopModule
        title-modifier="LATEST"
        title="STORY"
        link-to-more="/"
      >
        <div
          slot="topModuleBody"
          class="topBlog"
        >
          <h3 class="topBlog_title">
            <nuxt-link
              class="topBlog_link"
              to="/"
            >
              連記動詞だったり分離動詞だったり
            </nuxt-link>
          </h3>
          <p class="topBlog_date">
            2019/05/25 21:12
          </p>
          <p class="topBlog_body">
            ここのところやけにドイツ語にはまってしまっている. 大学 1 年のとき，第 2 外国語の選択でドイツ語を選んだのだが，先生がいわゆる変人で，それゆえに当時教えられたことは未だに強烈に印象に残っている. ドイツ語の言語そのものの面白さを説いていただき，講義はとてもわかりやすかった。しかしそ…
          </p>
        </div>
      </TopModule>
    </section>
    <section class="page_section">
      <TopModule
        title-modifier="RECENT"
        title="WORKS"
        link-to-more="/"
      >
        <ul
          slot="topModuleBody"
          class="worksList"
        >
          <li class="worksList_item">
            <nuxt-link
              class="worksList_link"
              to="/"
            >
              dummy
            </nuxt-link>
          </li>
          <li class="worksList_item">
            <nuxt-link
              class="worksList_link"
              to="/"
            >
              dummy
            </nuxt-link>
          </li>
          <li class="worksList_item">
            <nuxt-link
              class="worksList_link"
              to="/"
            >
              dummy
            </nuxt-link>
          </li>
          <li class="worksList_item">
            <nuxt-link
              class="worksList_link"
              to="/"
            >
              dummy
            </nuxt-link>
          </li>
        </ul>
      </TopModule>
    </section>
    <section class="page_section">
      <TopModule
        title-modifier="LATEST"
        title="PHOTO"
        link-to-more="/"
      >
        <nuxt-link
          slot="topModuleBody"
          class="topPhoto"
          to="/"
        >
          <img
            class="topPhoto_img"
            src="@/assets/img/ume.jpg"
            alt="recent photo"
          >
        </nuxt-link>
      </TopModule>
    </section>
    <section class="page_section">
      <TopModule
        title="ABOUT"
      >
        <div
          slot="topModuleBody"
          class="about"
        >
          <h3 class="about_name">
            Hironori Oka
          </h3>
          <p class="about_text">
            1987 年埼玉県生まれ．
          </p>
          <p class="about_text">
            大学・大学院で建築意匠を学ぶ．
          </p>
          <p class="about_text">
            卒業後，インターネット関連の企業に就職．メディア系サービスのフロントエンド開発，デザインを手がける．
          </p>
        </div>
      </TopModule>
    </section>
  </section>
</template>

<script>
import TopHeader from '@/components/modules/TopHeader'
import TopModule from '@/components/modules/TopModule'

export default {
  components: {
    TopHeader,
    TopModule
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/topBlog.scss';
@import '@/assets/scss/worksList.scss';
@import '@/assets/scss/topPhoto.scss';
@import '@/assets/scss/about.scss';

.page {
  &_section {
    padding: 40px 32px;
  }
}
</style>
