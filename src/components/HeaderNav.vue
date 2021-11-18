<template>
  <div class="nav">
    <div class="left-container"></div>
    <div class="center-container">
      <router-link to="/" class="title">Aylst</router-link>
    </div>
    <div class="right-container">
      <div class="display-name">
        G-01
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import { mapState, mapActions } from 'vuex';

  @Component({
    computed: {
      ...mapState([
        'isSignIn',
        'user',
      ]),
    },
    methods: {
      ...mapActions([
        'signIn',
      ]),
    },
  })
export default class HeaderNav extends Vue {}
</script>

<style lang="stylus" scoped>
  .nav
    /* --- layout --- */
    display flex
    justify-content center
    align-items center
    /* --- end --- */
    /* --- style --- */
    position fixed
    z-index 9999
    width 100%
    height 50px
    background-color #6155a9
    box-shadow 0px 2px 4px -1px rgba(0, 0, 0, 0.2),
    0px 4px 5px 0px rgba(0, 0, 0, 0.14),
    0px 1px 10px 0px rgba(0, 0, 0, 0.12)
    /* --- end --- */
    .left-container
      width 25%
    .center-container
      /*--- style ---*/
      width 50%
      /*--- end ---*/
      /*--- layout ---*/
      display flex
      justify-content center
      align-items center
      /*--- end ---*/
      .title
        font-size 24px
        font-weight 500
        color #fcdb65
        text-decoration none
        line-height 1.6
        letter-spacing 0.0075em
        &:hover
          cursor pointer
    .right-container
      /*--- style ---*/
      width 25%
      /*--- end ---*/
      /*--- layout ---*/
      display flex
      justify-content center
      align-items center
      /*--- end ---*/
      .display-name
        font-weight 500
        line-height 1.6
        letter-spacing 0.0075em
</style>
