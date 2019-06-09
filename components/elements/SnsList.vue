<template lang="html">
  <ul class="snsList">
    <li
      v-for="snsData in snsDataList"
      :key="snsData.name"
      class="snsList_item"
    >
      <a
        :href="snsData.url"
        class="snsList_link"
        target="_blank"
      >
        <font-awesome-icon
          :icon="[
            snsData.icon.type,
            snsData.icon.name
          ]"
        />
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      snsDataList: [
        {
          name: 'Twitter',
          url: 'https://twitter.com/offaxis1080mute',
          icon: {
            type: 'fab',
            name: 'twitter'
          }
        },
        {
          name: 'Instagram',
          url: 'https://www.instagram.com/hiro28/',
          icon: {
            type: 'fab',
            name: 'instagram'
          }
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.snsList {
  display: grid;
  grid-template-columns: repeat(2, 32px);
  column-gap: 20px;
  &_link {
    display: flex;
    align-items: center;
    justify-content: center;
    color: $white-l;
    line-height: 1;
    font: {
      size: 3.2rem;
    }
  }
}
</style>
