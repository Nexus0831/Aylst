<template>
  <div id="app">
    <HeaderNav class="header-nav"/>
    <router-view class="content"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Watch } from 'vue-property-decorator';
import HeaderNav from '@/components/HeaderNav.vue';

  @Component({
    components: {
      HeaderNav,
    },
  })
export default class App extends Vue {}
</script>

<style lang="stylus">
  #app
    height 100%
    display grid
    grid-template-rows 50px 1fr
    grid-template-columns 1fr
    font-family: 'Roboto', 'Noto Sans JP', sans-serif
    -webkit-font-smoothing antialiased
    -moz-osx-font-smoothing grayscale
    color #FFF
    @media(max-width 619px)
      /*grid-template-rows 50px 1fr*/
      grid-template-columns 16px 1fr 16px
    .header-nav
      /* --- position --- */
      grid-row 1 / 2
      grid-column 1 / 2
    /* --- end --- */
    .content
      grid-row 2 / 3
      grid-column 1/ 2
</style>
