<template>
  <section class="text">
    <div class="text__wrapper">
      <h3 class="text__subtitle">| Design+Lifestyle | Smart Living |</h3>
      <h2 class="text__title">
        Was hilft mir, Energie zu sparen und Spaß zu haben, bei mir zu Hause?
      </h2>
      <p class="text__description">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut dolor in reprehenderit in quia...
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Text'
}
</script>

<style lang="scss" scoped>
$text-color: #ffffff;

.text {
  width: 100px;
  height: 100px;
  background-color: #000;

  &__wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__subtitle {
    margin-bottom: 36px;
    font-size: 14px;
    font-weight: 500;
    color: $text-color;
    text-transform: uppercase;
  }

  &__title {
    margin-bottom: 37px;
    font-size: 24px;
    line-height: 30px;
    font-weight: 500;
    color: $text-color;
  }

  &__description {
    font-size: 12px;
    line-height: 1.2;
    font-weight: 400;
    color: $text-color;
  }
}
</style>
