<template>
    <div class="info-tabs">
        <nav>
            <div class="nav nav-tabs" id="nav-tab" role="tablist">
                <a class="nav-item nav-link active" id="nav-details-tab" data-toggle="tab" href="#nav-details" role="tab" aria-controls="nav-details" aria-selected="true">
                    Характеристики
                </a>
                <a class="nav-item nav-link" id="nav-description-tab" data-toggle="tab" href="#nav-description" role="tab" aria-controls="nav-description" aria-selected="false">
                    Описание
                </a>
                <a class="nav-item nav-link" id="nav-delivery-tab" data-toggle="tab" href="#nav-delivery" role="tab" aria-controls="nav-delivery" aria-selected="false">
                    Доставка
                </a>
                <a class="nav-item nav-link" id="nav-reviews-tab" data-toggle="tab" href="#nav-reviews" role="tab" aria-controls="nav-reviews" aria-selected="false">
                    Отзывы (0)
                </a>
            </div>
        </nav>
        <div class="tab-content" id="nav-tabContent">
            <div class="tab-pane fade show active" id="nav-details" role="tabpanel" aria-labelledby="nav-details-tab">
                <card-details/>
            </div>
            <div class="tab-pane fade" id="nav-description" role="tabpanel" aria-labelledby="nav-description-tab">
                <card-description/>
            </div>
            <div class="tab-pane fade" id="nav-delivery" role="tabpanel" aria-labelledby="nav-delivery-tab">
                <card-delivery/>
            </div>
            <div class="tab-pane fade" id="nav-reviews" role="tabpanel" aria-labelledby="nav-reviews-tab">
                <card-reviews/>
            </div>
        </div>
    </div>
</template>

<script>
    import cardDetails from "./card-info/card-details";
    import cardDescription from "./card-info/card-description";
    import cardDelivery from "./card-info/card-delivery";
    import CardReviews from "./card-info/card-reviews";

    export default {
        name: 'info-tabs',
        props: {},
        data() {
            return {}
        },
        computed: {},
        components: {
            CardReviews,
            cardDetails,
            cardDescription,
            cardDelivery
        }
    }
</script>