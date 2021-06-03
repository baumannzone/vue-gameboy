<template>
  <div class="game-boy">
    <div class="bg">
      <div class="box">
        <div class="cross-button" />
        <div class="a-b-button" />
        <div class="start-select-buttons" />
        <div class="speakers" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
};
</script>

<style scoped lang="stylus">
black-color = #413557
pink-color = #f96489

.game-boy
  display flex
  justify-content center
  padding 50px 0
  background: #f4f4f4

.box
  position relative
  width 220px
  height 350px
  border 21px solid black-color
  border-radius 25px 25px 50px 25px
  box-shadow 20px 0 0 0 black-color

  .cross-button
    position absolute
    height 60px
    width 20px
    background-color: black-color
    border-radius 5px
    bottom 50px
    left 30px

    &::before
      position absolute
      content ''
      width 100%
      height 100%
      background-color black-color
      border-radius 5px
      left 0
      transform rotate(90deg)

  .a-b-button
    position absolute
    width 75px
    height 30px
    bottom 80px
    right 15px
    transform rotate(-25deg)

    &::before
      content ''
      position absolute
      width 30px
      height 30px
      background pink-color
      left 0
      border-radius 50%
      box-shadow 45px 0 0 0 pink-color

  .start-select-buttons
    position absolute
    width 30px
    height 10px
    background-color: black-color
    border-radius 5px
    bottom 30px
    left 50px
    box-shadow 50px 0 black-color

  .speakers
    position absolute
    width 10px
    height 10px
    background-color: black-color
    border-radius 5px
    bottom 30px
    right 40px
    box-shadow 15px 0 black-color, 30px 0 black-color, 0 15px black-color, 15px 15px black-color, 30px 15px black-color
</style>
