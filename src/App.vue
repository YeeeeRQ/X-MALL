<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont icon-position"></span>
      <span class="position__info"
        >厦门理工学院 知行苑 X0X号厦门理工学院 知行苑 X0X厦门理工学院 知行苑
        X0X号号</span
      >
      <span class="iconfont icon-bell"></span>
    </div>
  </div>
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

<style lang="scss" scoped>
.wrapper {
  border: 1px solid red;
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0.55rem;
  right: 0;
  padding-left: 0.18rem;
  padding-right: 0.18rem;

  // background-color: lightgoldenrodyellow;
  .position {
    display: flex;
    padding: 0.16rem 0;
    font-size: 0.16rem;
    line-height: 0.16rem;
    color: #333;

    &__info {
      flex-grow: 1;

      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    }

    > .icon-position {
      font-size: 0.2rem;
      margin-right: 0.06rem;
    }

    > .icon-bell {
      font-size: 0.23rem;
      margin-left: 0.06rem;
    }
  }
}

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
