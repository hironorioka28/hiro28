<template lang="html">
  <div class="today">
    <p class="today_date">
      02
    </p>
    <p class="today_month">
      JUN
    </p>
    <p class="today_year">
      2019
    </p>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.today {
  text-align: center;
  line-height: 1;
  letter-spacing: 0;
  font: {
    weight: 100;
  }
  &_date {
    font: {
      size: 4.8rem;
    }
  }
  &_month {
    letter-spacing: 0.16em;
    font: {
      size: 2.4rem;
    }
  }
  &_year {
    font: {
      size: 2.4rem;
    }
  }
}
</style>
