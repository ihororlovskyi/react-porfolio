<template>
  <header class="main-menu">
    <nav class="main-menu__list">
      <nuxt-link v-touch-ripple class="main-menu__link" to='/' exact>
        <img class="main-menu__icon-eagle" src="/assets/img/svg-icons/old/ihororlovskyi.svg">
        About
      </nuxt-link>
      <nuxt-link v-touch-ripple class="main-menu__link" to='/portfolio'>Portfolio</nuxt-link>
      <nuxt-link v-touch-ripple class="main-menu__link" to='/contacts'>Contacts</nuxt-link>
    </nav>
  </header>
</template>

<style lang="scss">
.main-menu {
  background-color: #000;
  position: relative;
  z-index: 100;

  &__list {
    max-width: 555px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  &__link {
    font-weight: 600;
    text-transform: uppercase;
    padding: 1em 0;
    flex-basis: (100% / 3);
    transition: background-color .2s ease-in-out, color .2s ease-in-out;

    &.nuxt-link-active {
      background-color: #111;
    }
  }

  &__icon-eagle {
    width: 1.1em;
    transform: translateY(20.5%);
    margin-right: .5em;
  }
}
</style>
