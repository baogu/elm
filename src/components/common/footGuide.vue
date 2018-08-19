<template>
  <section id='foot_guide'>
    <mu-container>
      <mu-bottom-nav :value.sync="shift" @change="gotoAddress()">
        <mu-bottom-nav-item title="外卖" icon="restore"></mu-bottom-nav-item>
        <mu-bottom-nav-item title="搜索" icon="search"></mu-bottom-nav-item>
        <mu-bottom-nav-item title="订单" icon="assignment"></mu-bottom-nav-item>
        <mu-bottom-nav-item title="我的" icon="person"></mu-bottom-nav-item>
      </mu-bottom-nav>
    </mu-container>
  </section>
</template>

<script>
  import { mapState } from 'vuex'
  export default {
    name: "footGuide",
    data() {
      return {
        shift: 0
      }
    },
    created() {

    },
    computed: {
      ...mapState([
        'geohash'
      ]),
    },
    methods: {
      gotoAddress(){
        console.log(this.shift);
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../style/mixin';
  .container{
    padding: 0;
  }

  #foot_guide{
    background-color: #fff;
    position: fixed;
    z-index: 100;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    box-shadow: 0 -0.026667rem 0.053333rem rgba(0,0,0,.1);
  }
  .guide_item{
    flex: 1;
    display: flex;
    text-align: center;
    flex-direction: column;
    align-items: center;
    .icon_style{
      @include wh(.8rem, .8rem);
      margin-top: .3rem;
      fill: #ccc;
    }
    span{
      @include sc(.45rem, #666);
    }
  }

</style>
