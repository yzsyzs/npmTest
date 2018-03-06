<template>
    <div class="is-background">
      <p ref="isBack" @click="colorChange" :style="{background: isBackground}">我是测试插件</p>
    </div>
</template>
<script>
export default {
  name: 'vue-pay-keyboard',
  props: {
    isBackground: {
      type: String,
      default: '#ccc'
    }
  },
  data () {
    return {
    }
  },
  computed: {
  },
  mounted () {
    // this.$refs.isBack.style.background = this.isBackground
  },
  methods: {
    colorChange () {
      this.$emit('colorChange')
    }
  }
  // watch: {
  //   isBackground () {
  //     this.$refs.isBack.style.background = this.isBackground
  //   }
  // }
}
</script>
<style lang="scss" scoped>
.is-background {
  p {
    width: 200px;
    height: 200px;
  }
}
</style>