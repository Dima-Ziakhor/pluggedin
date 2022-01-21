<template>
  <section class="room">
    <Text/>
  </section>
</template>

<script>
import Text from './Text'

export default {
  name: 'Room',
  components: {
    Text
  }
}
</script>

<style lang="scss" scoped>
.room {
  background: url("../assets/images/section3-bg.png") center center / cover no-repeat;
  grid-column: 1 / 3;
}
</style>
