<template>
  <section class="inspiration">
    <h2 class="inspiration__title">A place called Inspiration.</h2>
    <p class="inspiration__description">
      Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam voluptatem.
    </p>

    <div class="inspiration__select-chart">
      <select class="inspiration__select" name="charts" id="charts">
        <option
          v-for="chart in charts"
          :key="chart"
          v-bind:value="chart"
        >
          {{ chart }}
        </option>
      </select>

      <button class="inspiration__insert">
        Insert
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Inspiration',
  data () {
    return {
      charts: [
        'Select chart type',
        'pie',
        'bar',
        'line'
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
$main-color: #fff;
@mixin selectStyles {
  height: 32px;
  width: 100%;
  border: 1px solid #fff;
  outline: none;
  background-color: transparent;
  font-size: 12px;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: 0.01em;
  color: #ffffff;
  cursor: pointer;
}

  .inspiration {
    font-family: "Open Sans", Helvetica, sans-serif;
    padding: 39px 41px 33px 32px;
    height: 400px;
    background-color: #323232;

    &__title {
      margin-bottom: 35px;
      font-size: 24px;
      line-height: 1.2;
      font-weight: 500;
      color: $main-color;
    }

    &__description {
      margin-bottom: 31px;
      font-size: 14px;
      line-height: 24px;
      font-weight: 400;
      color: $main-color;
    }

    &__select-chart {
      width: 152px;
    }

    &__select {
      @include selectStyles;

      margin-bottom: 9px;
    }

    &__insert {
      @include selectStyles;

      transition: background-color 0.3s;

      &:hover {
        background-color: rgba($color: #fff, $alpha: 0.5);
      }
    }
  }
</style>
