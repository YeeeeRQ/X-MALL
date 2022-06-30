<template>
    <div class="wrapper">
        <StaticPart/>
        <Nearby/>
    </div>
    <Docker/>
</template>

<script>
import Docker from './Docker';
import StaticPart from './StaticPart';
import Nearby from './Nearby';

export default {
    name: "Home",
    components: {
        StaticPart,
        Nearby,
        Docker,
    }
}
</script>

<style lang="scss" scoped>
.wrapper {
    overflow-y: auto;
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0.55rem;
    right: 0;
    padding: 0 0.18rem 0.3rem 0.18rem;
}
</style>
