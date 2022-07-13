<template>
<div class="smzq">
    <h1 @click="init" ref="box">{{packet}}</h1>
    <el-button type="primary" round>Primary</el-button>
</div>
</template>

<script>
export default {
  // data函数
  data () {
    return {
      packet: '我是data数据函数中的原始数据'
    }
  },
  // 创建前
  beforeCreate () {
    // data为undefined
    console.log('创建前')
    console.log(this.packet)
    console.log(this.$refs.box)
  },
  // 创建后
  created () {
    console.log('创建后')
    console.log(this.packet)
    console.log(this.$refs.box)
  },
  // 挂载前
  beforeMount () {
    console.log('挂载前')
    console.log(this.packet)
    console.log(this.$refs.box)
  },
  // 挂载后
  mounted () {
    console.log('挂载后')
    console.log(this.packet)
    console.log(this.$refs.box)
  },
  // 更新前
  beforeUpdate () {
    console.log('更新前')
    console.log(this.packet)
    console.log(this.$refs.box)
  },
  // 更新后
  updated () {
    console.log('更新后')
    console.log(this.packet)
    console.log(this.$refs.box)
  },
  activated () {

  },
  beforeUnmount () {
    console.log('卸载前')
  },
  unmounted () {
    console.log('卸载后')
  },
  methods: {
    init () {
      this.packet = ' 我是更新后的数据 '
      console.log(this.packet)
    }
  }
}
</script>

<style lang="less" scoped>
</style>
