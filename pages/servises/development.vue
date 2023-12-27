<script setup lang="ts">

import Develop from "~/components/Ui-elements/develop.vue";
</script>

<template>
  <div>
    <ui-elements-title-serv title="Разработка" sub-title="сайтов"  label-one="МАЛЫЙ БИЗНЕС" label-two="СРЕДНИЙ БИЗНЕС" label-three="ЭКСПЕРТЫ" podtitle="Когда нужно ускорить прирост клиентов. Здесь каждый начинает видеть перспективы и находит решение проблемы"/>
    <div class="develop">
      <develop type-off="Разработка" back="/image/main/caseOne.webp" title="Landing-Page" date="до 15 дней" description="Сайты-визитки для приема заявок"/>
      <develop type-off="Разработка" back="/image/main/caseTwo.webp" title="Интернет-магазин" date="от 30 дней" description="сложный интрнет-магазин с подключением онлайн-касс и собственной админ панелью"/>
      <develop type-off="Разработка" back="/image/main/caseThree.webp" title="Корпоративный сайт" date="до 30 дней" description="Многостраничный сайт с собственной админ панелью"/>
      <develop type-off="Разработка" back="/image/main/caseOne.webp" title="Личный блог" date="от 15 дней дней" description="Сайт с возможностью добавлять/редактировать/удалять Ваши публикации"/>
    </div>
  </div>
</template>

<style scoped lang="scss">
.develop{
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
.podtitle{

}
</style>