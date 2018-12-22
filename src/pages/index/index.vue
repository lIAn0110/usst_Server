<template>
<div>
    <i-tab-bar class="footer" current="index" color="#7690f9" @change="handleChange">
        <i-tab-bar-item key="index" icon="brush_fill" current-icon="brush_fill" title="报修"></i-tab-bar-item>
        <i-tab-bar-item key="chat" icon="interactive" current-icon="interactive" title="联系我们"></i-tab-bar-item>
        <i-tab-bar-item key="home" icon="homepage" current-icon="homepage" title="提交"></i-tab-bar-item>
    </i-tab-bar>
    <i-message id="message"/>
</div>
</template>

<script>
// src里面的.vue文件路径开始
const { $Message } = require('../../../dist/static/iview/base/index')

export default {
  data () {
    return {
      isShow: true
    }
  },
  created () {
    // 此处是获取不到组件的, 页面还没挂载
    // $Message({
    //   content: 'text',
    //   ctx: this
    // })
  },
  mounted () {
    // 请将页面元素相关的操作放在 mounted 中
    $Message({
      content: 'text'
    })
  },
  methods: {
    handleChange (event) {
      const page = event.mp.detail['key']
      const url = '../' + page + '/main'
      wx.navigateTo({ url })
    }
  }
}
</script>
