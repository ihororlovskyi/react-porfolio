<template>
  <div class="flex-sticky">
    <div class="flex-sticky__fractal">
      <Fractal/>
    </div>
    <div class="flex-sticky__header">
      <MainMenu/>
    </div>
    <div class="flex-sticky__content">
      <nuxt/>
    </div>
    <div class="flex-sticky__footer">
      <FooterBlock/>
    </div>
  </div>
</template>

<script>
import Fractal from '~/components/Fractal.vue'
import MainMenu from '~/components/MainMenu.vue'
import FooterBlock from '~/components/FooterBlock.vue'

export default {
  components: {
    Fractal,
    MainMenu,
    FooterBlock
  }
}
</script>

<style lang="scss">
// @import url('https://fonts.googleapis.com/css?family=Open+Sans:400,600&subset=cyrillic');
// @import '../node_modules/normalize.css/normalize.css';
$text-color: #ccc;
$link-color: darken($text-color, 15%);
$link-color-hover: lighten($link-color, 30%);

body {
  // font-family: 'Open Sans', sans-serif;
  font: 400 14px/1.5 "Lucida Grande","Tahoma","Verdana","Arial",sans-serif,"Roboto",Helvetica,Arial,sans-serif;
  text-align: center;
  background-color: #111;
  font-size: 16px;
  color: $text-color;
  margin: 0;
}

a {
  color: $link-color;
  text-decoration: none;
  outline: 0;
  transition: color .2s ease-in-out;

  &:hover,
  &:focus {
      color: $link-color-hover;
  }
}

img {
  max-width: 100%;
  display: inline-block;
}

html,
body,
#__nuxt,
#__layout {
  height: 100%;
}

.flex-sticky {
  min-height: 100%;
  display: flex;
  flex-direction: column;

  &__fractal {
  }

  &__header {
  }

  &__content {
    flex: 1;
    padding: 2em .6em;
    position: relative;
    // background-color: #000;
  }

  &__footer {
  }
}

// selection color
$selection-color: #8e44ad;

::selection {
  background: $selection-color;
}

::-moz-selection {
  background: $selection-color;
}

img::selection {
  background: transparent;
}

img::-moz-selection {
  background: transparent;
}

body {
  -webkit-tap-highlight-color: $selection-color;
}
</style>
