<template>
    <div class="cost__dev">
        <UiElementsTitle title="Стоимость разработки"/>

        <div class="cards">
            <UiElementsCostItem timeDay="Сроки 5-10 дней" title="Лэндинг" description="Для продаж и получения заявок" metaOne="Уникальный дизайн" metaTwo="Мобильная адаптация" metaThree="Создание бота в телеграм" metaFour="SEO оптимизация" cost="150$"/>
            <UiElementsCostItem timeDay="Сроки 9-17 дней" title="Интернет магазин" description="Для продаж товаров или услуг" metaOne="Уникальный дизайн" metaTwo="Мобильная адаптация" metaThree="Подключение CRM" metaFour="SEO оптимизация" metaFive="Добавление каталога" metaSix="Интеграция с 1С, Мой Склад, ВК" cost="230$"/>
            <UiElementsCostItem timeDay="Сроки 9-15 дней" title="Корпоративный" description="Для предоставления информации о компании ее товарах или услугах" metaOne="Уникальный дизайн" metaTwo="Мобильная адаптация" metaThree="Анализ продукта и конкурентов" metaFour="Разработка структуры" metaFive="SEO оптимизация" cost="180$" classCard="card__three"/>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
    .cost__dev{
        padding-top: 120px;
    }
    .cards{
        display: flex;
        justify-content: stretch;
        // flex-wrap: wrap;
        gap: 20px;
    }
    @media screen and (max-width: 800px) {
        .cards{
            flex-wrap: wrap;
            margin: 0 20px;
            justify-content: center;
        }
    }
</style>