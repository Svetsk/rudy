<template>
  <div class="footer" id="footer">
    <div>
      <a href="">Сайты под ключ</a>
      <a href="">Продвижение</a>
      <a href="">Портфолио</a>
      <a href="">Блог</a>
      <a href="">Этапы и оплата</a>
    </div>
    <div>
      <a href="https://t.me/Zakharssss">Telegram</a>
      <a href="viber://add?number=375299468676">Viber</a>
      <a href="">Instagram</a>
      <a href="https://vk.com/zakharrudy">Vk</a>
    </div>
    <div class="left__text">
      <a href="">+375 (29) 946-8676</a>
      <a href="">УНП: KM0109764</a>
      <a href="">RudyStudio@gmail.com</a>
      <nuxt-link class="pol__conf" to="/">Политика конфиденциальности</nuxt-link>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer {
  margin: 0 20px;
  padding: 120px 0;
  color: black;
  display: flex;
  flex-wrap: wrap;
  row-gap: 20px;
  justify-content: space-between;
  & div {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
  }
}
.left__text{
  text-align: end;
}
.pol__conf{
  padding-top: 66px;
}
@media screen and ( max-width:520px) {
  .footer {
    display: flex;
    flex-direction: column;
  }
  .left__text{
    text-align: start;
  }
}
</style>
