<template>
    <div>
        <!-- Main slider -->
        <splide :options="primaryOptions" ref="primary" class="swiper">
            <splide-slide>
                <img src="../../assets/img/products/img1.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img2.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img3.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img4.jpg">
            </splide-slide>

            <splide-slide>
                <img src="../../assets/img/products/img6.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img7.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img8.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img9.jpg">
            </splide-slide>
        </splide>

        <!-- Thumbnail slider -->
        <splide :options="secondaryOptions" ref="secondary" class="thumbnail-slider d-none d-md-flex">
            <splide-slide>
                <img src="../../assets/img/products/img1.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img2.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img3.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img4.jpg">
            </splide-slide>

            <splide-slide>
                <img src="../../assets/img/products/img6.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img7.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img8.jpg">
            </splide-slide>
            <splide-slide>
                <img src="../../assets/img/products/img9.jpg">
            </splide-slide>
        </splide>

    </div>
</template>

<script>
    import { Splide, SplideSlide } from '@splidejs/vue-splide';
    import '@splidejs/splide/dist/css/themes/splide-skyblue.min.css';

    export default {
        components: {
            Splide,
            SplideSlide,
        },
        data() {
            return {
                primaryOptions: {
                    type      : 'loop',
                    pagination: true,
                    arrows    : false,
                },
                secondaryOptions: {
                    type        : 'slide',
                    rewind      : true,
                    width       : 600,
                    gap         : '1rem',
                    pagination  : false,
                    fixedWidth  : 110,
                    fixedHeight : 70,
                    cover       : true,
                    focus       : 'center',
                    isNavigation: true,
                    arrows      : false,
                },
            };
        },

        mounted() {
            // Set the sync target.
            this.$refs.primary.sync( this.$refs.secondary.splide );
        },
    }
</script>
