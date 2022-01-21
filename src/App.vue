<template>
  <div id="app">
    <header class="header">
      <Nav/>
    </header>

    <main class="main">
      <div class="main__content">
        <Carusel/>
        <Inspiration/>
        <Room/>
        <Text/>
      </div>
    </main>
  </div>
</template>

<script>
import Nav from './components/Nav'
import Carusel from './components/Carusel'
import Inspiration from './components/Inspiration'
import Room from './components/Room'
import Text from './components/Text'

export default {
  name: 'App',
  components: {
    Nav,
    Carusel,
    Inspiration,
    Room,
    Text
  }
}
</script>

<style lang="scss" src="@/assets/styles/style.scss"></style>
