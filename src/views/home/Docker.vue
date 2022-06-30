<template>
    <div class="docker">
        <div v-for="(item, index) in dockerList" :key="item" class="docker__item"
            :class="{ 'docker__item--active': index === 0 }">
            <div class="iconfont" :class="'icon-' + item.iconClass"></div>
            <div class="docker__title">{{ item.text }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Docker",
    setup() {
        const dockerList = [
            { iconClass: 'home1', text: '首页' },
            { iconClass: 'cart-full', text: '购物车' },
            { iconClass: 'order', text: '订单' },
            { iconClass: 'my', text: '我的' }
        ]
        return { dockerList }
    }
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