<template>
  <transition name="modal-fade">
    <div class="kk__loading--wrap">
      <div class="kk__mask" v-if="fullScreen"></div>
      <div class="kk__loading" :class="[
            {'kk__loading--fullScreen':fullScreen}
            ]">
        <span class="kk__loading--loader" :class="[
            {'kk__loading--vertical':vertical,'borderRightTransparent':color}
            ]" :style="{'width': width+'px','height': height+'px','border-color': color,'border-width': borderWidth+'px'}"></span>
        <span class="kk__loading--text" v-if="hasText">
          <slot>加载中...</slot>
        </span>
      </div>
    </div>
  </transition>
</template>

<script>

export default {
  name: 'kk-loading',
  props: {
    color: {
      type: String,
      default: ''
    },
    width: {
      type: String,
      default: ''
    },
    height: {
      type: String,
      default: ''
    },
    borderWidth: {
      type: String,
      default: ''
    },
    fullScreen: {
      type: Boolean,
      default: false
    },
    hasText: {
      type: Boolean,
      default: false
    },
    vertical: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped lang="scss">

</style>
