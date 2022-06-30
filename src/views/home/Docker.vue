<template>
  <div class="docker">
    <div class="docker__item docker__item--active">
      <div class="iconfont icon-home1"></div>
      <div class="docker__title">首页</div>
    </div>
    <div class="docker__item">
      <div class="iconfont icon-cart-full"></div>
      <div class="docker__title">购物车</div>
    </div>
    <div class="docker__item">
      <div class="iconfont icon-order"></div>
      <div class="docker__title">订单</div>
    </div>
    <div class="docker__item">
      <div class="iconfont icon-my"></div>
      <div class="docker__title">我的</div>
    </div>
  </div>
</template>

<script>
export default {
    name: "Docker"
}
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixins.scss";
.docker {
  border-top: 1px solid #f1f1f1;
  // background-color: lightgreen;
  padding-top: 0.03rem;
  width: 100%;
  height: 0.55rem;
  padding-left: 0.18rem;
  padding-right: 0.18rem;
  position: absolute;
  left: 0;
  bottom: 0;
  color: $content-fontColor;

  display: flex;

  &__item {
    // border: 1px solid red;
    flex-grow: 1;
    font-size: 0.12rem;
    text-align: center;

    .iconfont {
      font-size: 0.28rem;
    }

    &--active {
      color: #07ac25;
    }
  }
}
</style>