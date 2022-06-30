<template>
    <div class="nearby">
        <h3 class="nearby__title">附近店铺</h3>

        <div class="nearby__item" v-for="item,index in nearbyList" :key="index">
            <img src="http://tva1.sinaimg.cn/large/007HyW8lly1h3pgfzdxgtj309a09ajt6.jpg" alt="nearby image"
                class="nearby__item__img" />
            <div class="nearby__content">
                <div class="nearby__content__title">{{ item.title }}</div>
                <div class="nearby__content__tags">
                    <div class="nearby__content__tag" v-for="tag in item.tags" :key="tag">{{ tag }}</div>
                </div>
                <p class="nearby__content__highlight">{{item.desc}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Nearby",
    setup() {
        const nearbyList = [
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3pgfzdxgtj309a09ajt6.jpg',
                title: '沃尔玛',
                tags: ['月售1万+', '起送￥0', '基础运费￥5'],
                desc: "VIP尊享满89元减4元运费券(每月3张)"
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3pgfzdxgtj309a09ajt6.jpg',
                title: '永辉超市',
                tags: ['月售2万+', '起送￥5', '基础运费￥6'],
                desc: "VIP尊享满89元减4元运费券(每月3张)"
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3pgfzdxgtj309a09ajt6.jpg',
                title: '天猫超市',
                tags: ['月售2万+', '起送￥5', '基础运费￥6'],
                desc: "VIP尊享满89元减4元运费券(每月3张)"
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3pgfzdxgtj309a09ajt6.jpg',
                title: '叮咚',
                tags: ['月售4万+', '起送￥5', '基础运费￥6'],
                desc: "VIP尊享满89元减4元运费券(每月3张)"
            },
        ]
        return { nearbyList }
    }
}
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixins.scss";

.nearby {
    &__title {
        margin: 0.16rem 0 0.12rem 0;
        font-size: 0.18rem;
        font-weight: normal;
        color: $content-fontColor;
    }

    &__item {
        display: flex;
        // border: 1px solid black;
        // padding: .12rem 0;
        padding-top: 0.12rem;
        border-bottom: 1px solid $content-bgColor;

        &__img {
            margin-right: 0.16rem;
            width: 0.56rem;
            height: 0.56rem;
        }
    }

    &__content {
        // border: 1px solid black;
        flex: 1;
        padding-bottom: 0.12rem;

        &__title {
            line-height: 0.22rem;
            font-size: 0.16rem;
            color: $content-fontColor;
        }

        &__tags {
            display: flex;
            margin-top: 0.08rem;
            line-height: 0.18rem;
            font-size: 0.13rem;
            color: $content-fontColor;
        }

        &__tag {
            margin-right: 0.16rem;
        }

        &__highlight {
            line-height: 0.18rem;
            font-size: 0.13rem;
            color: #e93b3b;
        }
    }
}
</style>