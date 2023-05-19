<template>
  <div class="flex flex-center wrapper">
    <q-card class="main-card">
      <q-card-section class="main-card__title">
        {{ lorem }}
      </q-card-section>
      <div class="q-pa-md q-gutter-sm main-card__btnGroup">
        <q-btn color="white" text-color="black" label="360p"/>
        <q-btn color="white" text-color="black" label="720p"/>
        <q-btn color="white" text-color="black" label="HD"/>
        <q-btn color="white" text-color="black" label="Full HD"/>
        <q-btn color="white" text-color="black" label="4K"/>
      </div>
    </q-card>
  </div>
  <div class="flex flex-center">
    <div class="list-item">
      <img alt="logo__numbOne" src="../assets/one.png" class="icon-numb">
      <q-card-section class="list-item__text">
        {{ lorem }}
      </q-card-section>
    </div>
    <div class="list-item">
      <img alt="logo__numbTwo" src="../assets/two.png" class="icon-numb">
      <q-card-section class="list-item__text">
        {{ lorem }}
      </q-card-section>
    </div>
    <div class="list-item">
      <img alt="logo__numbThree" src="../assets/three.png" class="icon-numb">
      <q-card-section class="list-item__text">
        {{ lorem }}
      </q-card-section>
    </div>
  </div>

</template>

<style lang="sass" scoped>
$colorTop: #f24d6e
$colorItem_text: #000
$widthIcon: 40px
$heightIcon: 40px

.wrapper
  width: 100%
  position: relative
  padding-bottom: 31%
  height: 300px
  align-items: baseline

.main-card
  position: absolute
  width: 800px
  height: 400px
  margin: 10px auto
  max-width: 80%
  max-height: 100%
  display: flex
  flex-direction: column
  justify-content: flex-end
  -webkit-clip-path: polygon(0 0, 0 100%, 100% 100%, 100% 30%, 85% 0)
  clip-path: polygon(0 0, 0 100%, 100% 100%, 100% 25%, 85% 0)
  background: $colorTop
  @media (max-width: 768px)
    width: 100%
  &__title
    width: 100%
    transform: translate(-50%, -50%)
    position: absolute
    left: 50%
    top: 50%
    color: #fff
    font-size: 24px
    display: -webkit-box
    -webkit-line-clamp: 3
    -webkit-box-orient: vertical
    overflow: hidden
    height: 135px
    @media (max-width: 768px)
      font-size: 26px
      -webkit-line-clamp: 2
      height: 100px
      top: 35%
  &__btnGroup
    display: flex
    align-items: flex-end
    justify-content: space-between
    overflow: hidden
    @media (max-width: 429px)
      flex-wrap: wrap

.list-item
  display: flex
  align-items: center
  width: 800px
  max-width: 80%
  padding: 5px 0
  &__text
    color: $colorItem_text

.icon-numb
  width: $widthIcon
  height: $heightIcon
</style>

<script>
export default {
  name: 'MainPage',
  setup() {
    return {
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
    }
  }
}
</script>
