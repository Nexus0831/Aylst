<template>
  <div id="home">
    <div class="main-content">
      <div class="content-title">
        <span class="neon-title">
          This is Aylst.
        </span>
        <br/>
        <span class="neon-text">
          Where my efforts converge.
        </span>
        <span class="content-body">
          This site contains a UI that I created for study purposes.
        </span>
      </div>
    </div>
    <div class="periodic-table">
      <ChemicalElement/>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ChemicalElement from '@/components/ChemicalElement.vue';

@Component({
  components: {
    ChemicalElement,
  },
})
export default class HomeView extends Vue {
}
</script>

<style lang="stylus" scoped>
#home
  display grid
  grid-template-rows 1fr
  grid-template-columns 1fr
  .main-content
    /** style start **/
    /** style end **/

    /** layout start **/
    display grid
    grid-template-rows 256px 1fr
    grid-template-columns 12px 1fr 12px
    /** layout end **/

    /** position start **/
    grid-row 2 / 3
    grid-column 1 / 2
    /** position end **/
  .content-title
    /** style start **/
    background-color #101010
    height 100%
    /** style end **/

    /** layout start **/
    display flex
    flex-direction column
    justify-content center
    align-items center
    /** layout end **/

    /** position start **/
    grid-row 1 / 2
    grid-column 1 / 4
    /** position end **/

  .neon-title
    blur = 1.75rem
    box-blur = calc(0.5 * blur)
    glow = #fcdb65

    color #000000
    -webkit-text-stroke 3px glow
    font-size 64px
    text-shadow 0 0 blur glow
    filter saturate(175%)

  .neon-text
    neon-text-color = #fcdb65
    animation flicker 1.5s infinite alternate
    font-size 24px

    @keyframes flicker
      0%, 19%, 21%, 23%, 25%, 54%, 56%, 100%
        text-shadow: -0.2rem -0.2rem 1rem #fff,
          0.2rem 0.2rem 1rem #fff,
          0 0 2rem neon-text-color,
          0 0 4rem neon-text-color,
          0 0 6rem neon-text-color,
          0 0 8rem neon-text-color,
          0 0 10rem neon-text-color

      20%, 24%, 55%
        text-shadow none
        /*box-shadow none*/

  .content-body
    /** style start **/
    padding 12px
    font-size 24px
    font-weight normal
    /** style end **/

    /** layout start **/
    /** layout end **/

    /** position start **/
    /** position end **/
  .periodic-table
    padding 12px
    background-color #303030
    /** position start **/
    grid-row 3 / 4
    grid-column 1 / 2
    /** position end **/
</style>
