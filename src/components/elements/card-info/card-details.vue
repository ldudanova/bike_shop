<template>
    <div class="card-details">
        <div class="card-details__group">
            <h3 class="card-details__title subtitle-1">
                Основные характеристики
            </h3>
            <div class="options-list">
                <div class="options-list__item">
                    <div class="options-list__label">Производитель</div>
                    <div class="options-list__value">Subrosa</div>
                </div>
                <div class="options-list__item">
                    <div class="options-list__label">Вес, гр.</div>
                    <div class="options-list__value">10360</div>
                </div>
                <div class="options-list__item">
                    <div class="options-list__label">Год</div>
                    <div class="options-list__value">2021</div>
                </div>
                <div class="options-list__item">
                    <div class="options-list__label">Рама</div>
                    <div class="options-list__value">Сталь / 1020 Hi-Ten / Ростовка 14.5" / Наклон рулевой трубы 74° / Наклон подседельной трубы 71° / Длина перьев 10.2" / Высота каретки 8.5" / Standover 6."</div>
                </div>
                <div class="options-list__item">
                    <div class="options-list__label">Вилка</div>
                    <div class="options-list__value">Сталь / 1020 Hi-Ten / Выбег 30мм / Дропауты 10мм / Конические ноги</div>
                </div>

                <a class="collapse-toggle iconic-text iconic-text_left link link_default collapse-toggle_show" data-toggle="collapse"
                   href="#collapseAllDetails" role="button"
                   aria-expanded="false" aria-controls="collapseAllDetails">
                    <span class="collapse-toggle__text collapse-toggle__text_show">Все характеристики</span>
                    <svg class="iconic-text__icon" width="11" height="8" viewBox="0 0 11 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M10.1568 0.930194C10.5473 1.32072 10.5473 1.95388 10.1568 2.34441L5.5 7.00116L0.843247 2.34441C0.452723 1.95388 0.452723 1.32072 0.843247 0.930193C1.23377 0.539669 1.86694 0.539669 2.25746 0.930193L5.5 4.17273L8.74254 0.930194C9.13306 0.53967 9.76623 0.53967 10.1568 0.930194Z" fill="currentColor"/>
                    </svg>
                </a>

                <!--  Collapsing area  -->
                <div class="collapse" id="collapseAllDetails">
                    <div class="options-list__item">
                        <div class="options-list__label">Вынос</div>
                        <div class="options-list__value">Rant Alloy Top Load</div>
                    </div>
                    <div class="options-list__item">
                        <div class="options-list__label">Руль</div>
                        <div class="options-list__value">Сталь / 1020 Hi-Ten / Высота 6.0"</div>
                    </div>
                    <div class="options-list__item">
                        <div class="options-list__label">Цепь</div>
                        <div class="options-list__value">Rant Max 410</div>
                    </div>
                    <div class="options-list__item">
                        <div class="options-list__label">Подвеска</div>
                        <div class="options-list__value">Отсутствует</div>
                    </div>
                </div>

                <a class="collapse-toggle iconic-text iconic-text_left link link_default collapse-toggle_hide" data-toggle="collapse"
                   href="#collapseAllDetails" role="button"
                   aria-expanded="false" aria-controls="collapseAllDetails">
                    <span class="collapse-toggle__text collapse-toggle__text_hide">Скрыть характеристики</span>
                    <svg class="iconic-text__icon" width="11" height="8" viewBox="0 0 11 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M10.1568 0.930194C10.5473 1.32072 10.5473 1.95388 10.1568 2.34441L5.5 7.00116L0.843247 2.34441C0.452723 1.95388 0.452723 1.32072 0.843247 0.930193C1.23377 0.539669 1.86694 0.539669 2.25746 0.930193L5.5 4.17273L8.74254 0.930194C9.13306 0.53967 9.76623 0.53967 10.1568 0.930194Z" fill="currentColor"/>
                    </svg>
                </a>
            </div>
        </div>
        <div class="card-details__group">
            <h3 class="card-details__title subtitle-1">
                Комплект
            </h3>
            <div class="complect-table">
                <table>
                    <thead>
                    <tr>
                        <th>Упаковка</th>
                        <th>Размеры</th>
                        <th>Вес</th>
                    </tr>
                    </thead>
                    <tbody>
                    <tr>
                        <td data-label="Упаковка">Коробка №1</td>
                        <td data-label="Размеры">138см x 2см x 80см</td>
                        <td data-label="Вес">4.8 кг</td>
                    </tr>
                    <tr>
                        <td data-label="Упаковка">Коробка №2</td>
                        <td data-label="Размеры">201см x 7см x 25см</td>
                        <td data-label="Вес">5.5 кг</td>
                    </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'card-details',
        props: {},
        data() {
            return {}
        },
        computed: {}
    }
</script>

<style lang="scss">
    .card-details{
        &__title{
            margin-bottom: 16px;
        }
        &__group{
            margin-bottom: 40px;
        }
    }
    .complect-table{
        max-width: 325px;
        box-sizing: border-box;
        table{
            width: 100%;
        }
        th{
            box-sizing: border-box;
            border-bottom: 1px solid #e6e4e7;
            color: #a2a0a3;
            padding-bottom: 8px;
            font-weight: 400;
        }
        td{
            box-sizing: border-box;
            padding: 8px 0 4px;
        }
    }
</style>