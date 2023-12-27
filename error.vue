<template>
    <div>
        <UiAddHeader />
        <div class="error__wrapper">

            <div class="error">
                <strong>404</strong>
                <p>Мы не нашли страницы по вашему запросу</p>
                <div>
                    <nuxt-link to="/">Главная страница</nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.error{ 
    padding-top: 120px;
    display: flex;
    flex-direction: column;
    row-gap: 40px;
    justify-content: center;
    align-items: center;
    text-align: center;
}
    strong{
        color: #1536DF;
        font-family: 'Museo Sans Cyrl 500';
        font-size: 128px;
        font-style: normal;
        font-weight: 400;
        line-height: 109.8%; /* 140.544px */
    }
    p{
        color: #767676;
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        font-family: 'Inter';
        display: inline-block;
    }
    a{
        color: #FFF;
        font-family: 'Inter';
        font-size: 16px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        padding: 14px 81px;
        border-radius: 5px;
        background: #1536DF;
    }
</style>