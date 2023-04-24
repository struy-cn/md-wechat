<template>
  <el-dialog
    title="关于"
    class="about__dialog"
    :visible="visible"
    @close="$emit('close')"
    width="30%"
    center
  >
    <div style="text-align: center">
      <h3>一款高度简洁的微信 Markdown 编辑器，基于<a href="">doocs/md</a></h3>
      <p>
        欢迎关注我的公众号
        StruggleYang，持续分享有价值的工具、技术、好物与书籍！
      </p>
      <img
        src="https://img.struy.cn/img/202304212313349.png"
        style="width: 40%"
      />
    </div>
    <template slot="footer">
      <el-button
        type="primary"
        @click="onRedirect('https://github.com/struy-cn/md-wechat')"
        plain
      >
        GitHub 仓库
      </el-button>
      <el-button type="primary" @click="onRedirect('https://struy.cn/')" plain>
        个人博客
      </el-button>
    </template>
  </el-dialog>
</template>

<script>
export default {
  props: {
    visible: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    onRedirect(url) {
      window.open(url)
    },
  },
}
</script>

<style lang="less" scoped>
/deep/ .el-dialog {
  min-width: 420px;
}
</style>
