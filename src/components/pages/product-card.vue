<template>
    <div class="product-card">
        <Breadcrumbs/>
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

                            </div>
                        </div>
                        <div class="custom-photos"></div>
                    </div>
                </div>
                <div class="product-card__column product-card__column_right"></div>
                <div class="product-card__column product-card__column_left">
                    <div class="product-card__info">
                        <div class="info-tabs">
                            <nav></nav>
                            <div class="tab-content" id="nav-tabContent"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Breadcrumbs from '../elements/Breadcrumbs'

    export default {
        name: 'product-card',
        props: {},
        data() {
            return {}
        },
        computed: {},
        components: {
            Breadcrumbs,

        }
    }
</script>

<style lang="scss">
    .product-card{
        width: 100%;
        height: 100%;

    }
</style>