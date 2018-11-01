<template>
  <div class="wrap">

    <h2>基础组件</h2>
    <h4>按钮</h4>
    <kk-button>普通</kk-button>
    <kk-button type="primary" @click="btnClick" icon="kk__icon--checked">主要</kk-button>
    <kk-button type="error" icon="kk__icon--checked"></kk-button>
    <kk-button type="warning" disabled>禁止</kk-button>
    <kk-button plain>简约</kk-button>
    <kk-button type="text" icon="kk__icon--checked">文字</kk-button>
    <kk-button loading type="success">loading状态</kk-button>
    <kk-button bg-color="#fc0" color="#e0439a" border-color="#fc0">自定义颜色</kk-button>
    <br/><br/>
    <kk-button bg-color="#fcb" color="#e0439a" border-color="#fcb" block no-radius class="btn__block">无圆角块状</kk-button>
    <br/>
    <kk-button round long>100%宽圆角</kk-button>
    <br/><br/>
    <kk-button-group class="btn__group">
      <kk-button type="warning">警告</kk-button>
      <kk-button type="primary" @click="btnClick" icon="kk__icon--checked">主要</kk-button>
      <kk-button type="success" icon="kk__icon--loading">成功</kk-button>
    </kk-button-group>

    <h4>Toast</h4>
    <kk-button type="success" @click="toastClick1">文字</kk-button>
    <kk-button type="primary" @click="toastClick2">loading</kk-button>
    <kk-button type="error" @click="toastClick3">无遮罩</kk-button>

  </div>
</template>

<script>
export default {
  methods: {
    btnClick() {
      alert('按钮点击')
    },
    toastClick1() {
      this.$toast.text({ content: '太长会换行呢，15个字以内最好', direction: 'bottom' })
    },
    toastClick2() {
      this.$toast.loading({
        // mask: false
      })
    },
    toastClick3() {
      this.$toast.loading({
        mask: false
      })
    }
  }

}
</script>

<style lang="scss">

</style>

