/**
* Created by OXOYO on 2018/4/2.
*
* 图标组件
*/

<style scoped lang="less" rel="stylesheet/less">

</style>

<template>
  <i :class="classNameList"></i>
</template>

<script>
import './iconfont.css'
export default {
  name: 'Icon',
  props: {
    type: {
      type: String,
      required: true
    }
  },
  data () {
    return {
      className: {
        main: 'iconfont',
        prefix: 'xhv-icon-'
      }
    }
  },
  computed: {
    classNameList: function () {
      let _t = this
      let classNameByType = _t.type ? _t.className.prefix + _t.type : ''
      return [_t.className.main, classNameByType]
    }
  }
}
</script>
