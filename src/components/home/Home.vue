<template>
  <div>
    <HeadTop></HeadTop>
    <section class="homeComtainer">
      121
    </section>
    <FootGuide></FootGuide>
  </div>
</template>

<script>
  import HeadTop from "@/components/common/headTop"
  import FootGuide from "@/components/common/footGuide"
  export default {
    name: "Home",
    created() {
      this.axios.post("/userInfo").then((response) => {
        console.log(response)
      })
    },
    components: {
      HeadTop,
      FootGuide
    }
  }
</script>

<style scoped lang="scss">
  .homeComtainer{
    padding-top: 0px;
    height: 20000px;
    padding-bottom:56px;
  }
</style>
