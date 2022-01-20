<template>
  <nav id="nav" class="nav">
    <div class="nav__container">
      <div class="nav__logo-block">
        <div class="nav__logo">
          <a href="#" class="nav__logo-link">
            <img src="@/assets/images/logo.png" alt="logo">
          </a>
        </div>
        <div class="nav__slogan">
          <span>Inform.</span>
          <span>Connect.</span>
          <span>Inspire. </span>
        </div>
      </div>

      <div class="nav__menu">
        <div class="nav__info">
          <a href="#" class="nav__about-us nav__about">Über uns</a>
          <a href="#" class="nav__redaction nav__about">Redaktion</a>

          <div class="nav__switch-lang">
            <button class="nav__lang" disabled>de</button>
            <button class="nav__lang">en</button>
          </div>
        </div>

        <div class="nav__menu-block">
          <a href="#" class="nav__search">
            <img src="@/assets/images/search.png" alt="Search">
          </a>

          <ul class="nav__menu-list">
            <li
              v-for="item in menuList"
              :key="item"
              class="nav__item"
            >
              <a href="#" class="nav__link">{{ item }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
  data () {
    return {
      menuList: [
        '|',
        'Design+lifestyle',
        '|',
        'Trends',
        '|',
        'Infodelight',
        '|',
        'Smart Living'
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
$link-color: #333333;

.nav {
  font-family: "Open Sans", Helvetica, sans-serif;

  &__container {
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    padding: 20px 35px 12px;
    max-width: 1200px;
  }

  &__logo-block {
    padding-top: 31px;
    width: 163px;
  }

  &__logo {
    margin-bottom: 13px;
  }

  &__slogan {
    display: flex;
    justify-content: space-between;
    font-size: 14px;
    color: #323232;
    font-weight: 300;
  }

  &__info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 234px;
    margin: 0 0 40px auto;
  }

  &__about {
    font-size: 14px;
    color: $link-color;
    text-decoration: none;

    &:nth-child(1) {
      margin-right: 25px;
    }

    &:nth-child(2) {
      margin-right: 19px;
    }
  }

  &__switch-lang {
    display: flex;
  }

  &__lang {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 31px;
    height: 25px;
    border: 1px solid #000;
    background-color: transparent;
    font-family: "Open Sans", Helvetica, sans-serif;
    font-size: 14px;
    color: $link-color;
    text-transform: uppercase;
    cursor: pointer;

    &:first-child {
      opacity: 0.3;
    }
  }

  &__menu-block {
    display: flex;
    align-items: center;
    gap: 25px;
  }

  &__search {
    display: block;
    align-self: flex-end;
  }

  &__menu-list {
    display: flex;
    justify-content: space-between;
    list-style: none;
    width: 620px;
  }

  &__link {
    display: block;
    font-size: 16px;
    letter-spacing: 0px;
    line-height: 38px;
    color: $link-color;
    text-decoration: none;
    text-transform: uppercase;
  }
}
</style>
