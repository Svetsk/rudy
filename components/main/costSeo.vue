<template>
    <div class="cost__seo">
        <UiElementsTitle title="Стоимость продвижения" />

        <div class="costSeo__flex">
            <UiElementsCostItem title="SEO оптимизация" description="SEO продвижение подойдет для проектов которые работают в долгосрочной перспективе" metaOne="Создание сематического ядра" metaTwo="Внутренняя оптимизация сайта" metaThree="Внешняя оптимизация сайта" cost="105$"/>
            <UiElementsCostItem title="Контекстное" description="Контекстное продвижение позволит запустить продажи и получить первые заявки спустя 3 дня" metaOne="Подбор ключевых слов" metaTwo="Настройка рекламных компаний" metaThree="Анализ и подбор Целевой аудитории" metaFour="Настройка целей и конверсий" cost="80$"/>
            <UiElementsCostItem title="Копирайтинг" description="Составим текст для вашего сайта, блога, соц сетей. Пишем тексты для любой ниши" metaOne="Анализ сферы деятельности ( продукта )" metaTwo="Подбор ключевых слов" metaThree="Написание текста" cost="10$"/>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
    .cost__seo{
        padding-top: 120px;
    }
    .costSeo__flex{
        display: flex;
        column-gap: 20px;
        row-gap: 20px;
    }
    @media screen and (max-width: 800px) {
        .costSeo__flex{
            flex-wrap: wrap;
            margin: 0 20px;
            justify-content: center;
        }
    }
</style>