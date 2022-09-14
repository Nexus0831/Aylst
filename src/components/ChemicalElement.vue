<template>
  <div class="element">
    <span class="number">
      79
    </span>
    <span class="symbol">
      Au
    </span>
    <span class="name">
      Aurum
    </span>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class ChemicalElement extends Vue {}
</script>

<style lang="stylus" scoped>
  .element
    blur = 1.75rem
    box-blur = "calc(0.5 * %s)" % blur
    glow = #fcdb65
    size = 128px

    align-items center
    border-radius 12px
    border 4px solid currentColor
    box-shadow: inset 0 0 0 2px rgba(0, 0, 0, 0.15),
        0 0 0 2px rgba(0, 0, 0, 0.15),
      inset 0 0 box-blur glow,
        0 0 box-blur glow
    color glow
    display: inline-flex;
    flex-direction: column;
    /*font-family: system-ui, sans-serif;*/
    height: size;
    justify-content: space-around;
    padding: 1rem;
    width: size;

    .number
      font-weight 700

    .symbol

      color #000000
      -webkit-text-stroke 3px glow
      font-size 4rem
      text-shadow 0 0 blur glow
      filter saturate(175%)
</style>
