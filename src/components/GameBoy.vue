<template>
  <div class="game-boy">
    <div class="bg">
      <div class="box box-0"></div>
      <div class="box box-1">
        <div class="dots">
          <div class="dot"></div>
        </div>
        <div class="squares">
          <div class="square"></div>
        </div>
        <div class="pipe"></div>
        <div class="bricks">
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
          <div class="brick"></div>
        </div>
        <div class="cross-button" />
        <div class="a-b-buttons" />
        <div class="start-select-buttons" />
        <div class="speakers" />
      </div>
    </div>
  </div>
</template>

<script>
// Source: https://dribbble.com/shots/14194728-Doo-Doo-Doot
export default {
  name: "GameBoy",
};
</script>

<style scoped lang="stylus">
black-color = #413557
pink-color = #f96489
purple-color = #b5a2e1
green-color = #79f1bb

.game-boy
  display flex
  justify-content center
  padding 50px 0
  background: #f4f4f4

.bg
  display flex
  justify-content center

.box
  position relative
  width 325px
  height 485px
  border-radius 35px 35px 50px
  border 30px solid black-color
  background white

  &.box-0
    left 40px
    background black-color

  .pipe
    width 50px
    height 70px
    border 15px solid black-color
    top 120px
    right 50px
    background: green-color


  .dots
    position absolute
    .dot
      position relative
      width 13px
      height 13px
      background-color transparent
      border-radius 50%

  .bricks
    position absolute
    display flex
    width 160%
    height 45px
    top 50%
    left 50%
    padding 12px
    border-radius 5px
    transform translate(-50%, -50%)
    background-color black-color
    .brick
      width 45px
      height 45px
      margin-right 12px
      background-color pink-color

      &:last-child
        margin-right 0


  .cross-button
    position absolute
    width 30px
    height 90px
    bottom 80px
    left 45px
    background-color: black-color
    border-radius 8px

    &::before
      position absolute
      content ''
      width 100%
      height 100%
      left 0
      transform rotate(90deg)
      border-radius 5px
      background-color black-color

  .a-b-buttons
    position absolute
    width 125px
    height 45px
    bottom 100px
    right 30px
    transform rotate(-25deg)
    transform-origin left center

  .start-select-buttons
    position absolute
    width 35px
    height 12px
    bottom 45px
    left 50%
    transform translate(-170%)
    border-radius 12px
    background-color: black-color

  .speakers
    position absolute
    width 10px
    height 10px
    right 75px
    bottom 40px
    transform-origin left top
    border-radius 50%
    background-color black-color
</style>
