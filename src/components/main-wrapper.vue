<template>
    <div class="main-wrapper">

        <product-card></product-card>

    </div>
</template>

<script>
    import productCard from './pages/product-card'

    export default {
        name: 'main-wrapper',
        components: {
            productCard
        },
        props: {},
        data() {
            return {
            }
        },
        computed: {},
        methods: {},
        watch: {},
        mounted() {
        }
    }
</script>

<style lang="scss">
    .main-wrapper{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin: 0 auto;
        padding-top: 80px;
    }
</style>