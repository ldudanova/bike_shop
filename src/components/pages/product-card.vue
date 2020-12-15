<template>
    <div class="product-card">
        <div class="wrapper product-card__breadcrumbs">
        <Breadcrumbs/>
        </div>
        <div class="wrapper product-card__title">
            <h1 class="h1">SUBROSA ALTUS 14" 2021 BMX BIKE</h1>
        </div>
        <div class="wrapper">
            <div class="product-card__grid">
                <div class="product-card__column product-card__column_left">
                    <div class="product-card__photo-container">

                        <!--Swiper-->
                        <div class="product-slider">
                            <div class="swiper-container">
                                <SwiperSlider/>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="product-card__column product-card__column_right">
                    <!--  Aside panel START  -->
                        <aside-panel/>
                    <!--  Aside panel END    -->
                </div>
                <div class="product-card__column product-card__column_left">
                    <div class="product-card__info">
                        <info-tabs/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Breadcrumbs from '../elements/Breadcrumbs'
    import SwiperSlider from '../elements/SwiperSlider.vue';
    import infoTabs from '../elements/info-tabs.vue';
    import AsidePanel from "../elements/aside-panel";


    export default {
        name: 'product-card',
        props: {},
        data() {
            return {}
        },
        computed: {},
        components: {
            AsidePanel,
            Breadcrumbs,
            SwiperSlider,
            infoTabs
        }
    }
</script>

<style lang="scss">

</style>