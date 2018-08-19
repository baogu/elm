<template>
  <div id='head_top'>
    <mu-appbar style="width: 100%;" color="primary">
      <mu-button icon slot="left">
        <mu-icon value="menu"></mu-icon>
      </mu-button>
      首页
      <mu-button flat slot="right">登录|注册</mu-button>
    </mu-appbar>
  </div>
</template>

<script>
  import '../../static/iconfont/iconfont.css'
  export default {
    name: "headTop",
    data() {
      return {
        signinUp: true,
        userInfo: {},
        headTitle: "12"
      }
    },
    methods: {
      goBack() {

      }
    }
  }
</script>

<style scoped lang="scss">
  @import '../../style/mixin';
  #head_top{
    background-color: $blue;
    position: fixed;
    z-index: 100;
    left: 0;
    top: 0;
    text-align: center;
  @include wh(100%, 1.95rem);
  }
  .head_goback{
    left: 0.4rem;
    color: #fff;
  @include wh(0.6rem, 1rem);
    line-height: 2.2rem;
    margin-left: .4rem;
  }
  .head_login{
    right: 0.55rem;
  @include sc(0.65rem, #fff);
  @include ct;
  .login_span{
    color: #fff;
  }
  .user_avatar{
    fill: #fff;
  @include wh(.8rem, .8rem);
  }
  }
  .title_head{
  @include center;
    width: 50%;
    color: #fff;
    text-align: center;
  .title_text{
  @include sc(0.8rem, #fff);
    text-align: center;
    font-weight: bold;
  }
  }
</style>
