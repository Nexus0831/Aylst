<template>
  <div id="home">
    <div class="main-content">
      <div class="content-title">
        This is Aylst.
        <br/>
        Where my efforts converge.
        <span class="content-body">This site contains a UI that I created for study purposes.</span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
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
    background-color #6155a9
    color #fcdb65
    font-size 64px
    font-weight bold
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
</style>
