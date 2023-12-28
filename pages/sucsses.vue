<template>
    <div class="flet">
        <h1>Ваша заявка успешно<br>отправлена</h1>
        <p>Мы ответим вам в течении 20 минут! Так же вы можете<br>пройти тест в нашем Telegram-боте и получить скидку</p>
        <div>
            <a href="https://t.me/RudyStudioBrif_bot">Получить скидку</a>
        </div>
        <NuxtImg src="/image/sucsses.svg" width="606px" height="446px" />
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.flet{
    position: relative;
    margin: 0 20px;
    display: flex;
    flex-direction: column;
    gap: 40px;
    padding: 58px 0 200px;
    & *{
        margin: 0;
        padding: 0;
    }
}
h1{
    color: #000;
    font-family: 'Museo Sans Cyrl 500';
    font-size: 60px;
    font-weight: 400;
    line-height: 109.8%; /* 65.88px */
}
p{
    color: #767676;
    font-family: 'Inter';
    font-size: 24px;
    font-weight: 400;
}
a{
    border-radius: 5px;
    background: #1536DF;
    padding: 14px 81px !important;
    color: #FFF;
    font-family: 'Inter';
    font-size: 16px;
    font-weight: 700;
}
img{
    position: absolute;
    right: 0;
}
@media screen and (max-width: 1200px) {
    h1{
        padding-bottom: 446px !important;
    }
    img{
        left: 0;
        top: 200px;
    }
}
@media screen and (max-width: 800px) {
    h1{
        color: #000;
        font-size: 36px;
        font-weight: 400;
        line-height: 109.8%; /* 39.528px */
        padding-bottom: 300px !important;
    }
    p{
        font-size: 16px;
        font-weight: 400;
    }
    a{
        padding: 14px 81px;
    }
    img{
        width: 338px;
        height: 337px;
    }
}
</style>