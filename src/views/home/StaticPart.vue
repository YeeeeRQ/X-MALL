<template>
    <div class="position">
        <span class="iconfont icon-position"></span>
        <span class="position__info">厦门理工学院 知行苑 X0X号厦门理工学院 知行苑 X0X厦门理工学院 知行苑
            X0X号号</span>
        <span class="iconfont icon-bell"></span>
    </div>
    <div class="search">
        <span class="iconfont icon-fenxiang"></span>
        <!-- <input type="text" class="search__keywords" /> -->
        <span class="search__keywords">永辉会员商店优惠商品</span>
    </div>
    <div class="banner">
        <img src="//img12.360buyimg.com/img/s750x205_jfs/t1/126041/16/23560/25488/62b29ffdE10c1ab86/9463e6b699976153.jpg!q70.dpg.webp"
            alt="banner img" />
    </div>
    <div class="icons">
        <div class="icons__item" v-for="item in iconList" :key="item.desc">
            <img class="icons__item__img" :src="item.imgUrl" />
            <p class="icons__item__desc">{{ item.desc }}</p>
        </div>

    </div>
    <div class="gap"></div>

</template>

<script>
export default {
    name: "StaticPart",
    setup() {
        const iconList = [
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p55ipms9j30280280sq.jpg',
                desc: '超市便利'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lg20slj3028028aa2.jpg',
                desc: '菜市场'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lfwtu5j3028028aa3.jpg',
                desc: '水果店'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lg543kj30280283yh.jpg',
                desc: '鲜花绿植'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lg0mudj3028028mx6.jpg',
                desc: '医药健康'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lfwau0j3028028jrd.jpg',
                desc: '家居时尚'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lfy6zsj30280280sr.jpg',
                desc: '烘焙蛋糕'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lfvlsej302802874b.jpg',
                desc: '签到'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lfvgnaj3028028jrd.jpg',
                desc: '大牌免运'
            },
            {
                imgUrl: 'http://tva1.sinaimg.cn/large/007HyW8lly1h3p5lfvebnj302802874a.jpg',
                desc: '红包套餐'
            },
        ]
        return { iconList }
    }
}
</script>


<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixins.scss";

.position {
    display: flex;
    padding: 0.16rem 0;
    font-size: 0.16rem;
    line-height: 0.16rem;
    color: $content-fontColor;

    &__info {
        flex-grow: 1;

        @include ellipsis;
    }

    >.icon-position {
        font-size: 0.2rem;
        margin-right: 0.06rem;
    }

    >.icon-bell {
        font-size: 0.23rem;
        margin-left: 0.06rem;
    }
}

.search {
    // border: 1px solid red;
    color: #b7b7b7;
    background-color: #f5f5f5;
    border-radius: 0.2rem;
    font-size: 0.16rem;
    line-height: 0.32rem;
    margin-top: 0.08rem;
    margin-bottom: 0.12rem;
    padding-top: 0.03rem;
    padding-bottom: 0.03rem;

    display: flex;

    >.iconfont {
        margin-left: 0.12rem;
        margin-right: 0.12rem;
    }

    &__keywords {
        // border: 1px solid black;
        flex-grow: 1;
        margin-right: 0.12rem;
        @include ellipsis;
    }
}

.banner {
    height: 0;
    overflow: hidden;
    padding-bottom: 27.3%;
}

.icons {
    // border: 1px solid red;
    display: flex;
    flex-wrap: wrap;
    margin-top: 0.15rem;

    &__item {
        // display: flex;

        // border: 1px solid red;
        width: 20%;

        &__img {
            display: block;
            width: 0.46rem;
            height: 0.46rem;
            margin: 0 auto;
        }

        &__desc {
            padding-bottom: 0.1rem;
            text-align: center;
            color: $content-fontColor;
        }
    }
}


.gap {
    margin: 0 -0.18rem;
    height: 0.1rem;
    background-color: #f1f1f1;
}
</style>