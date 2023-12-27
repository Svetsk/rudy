<script setup lang="ts">

import Develop from "~/components/Ui-elements/develop.vue";
</script>

<template>
  <div>
    <ui-elements-title-serv title="Дизайн" sub-title="под ключ"  label-one="МАЛЫЙ БИЗНЕС" label-two="СРЕДНИЙ БИЗНЕС" label-three="ЭКСПЕРТЫ" podtitle="Когда нужно привлеч новых лидов. Здесь каждый начинает видеть перспективы"/>
    <div class="develop">
      <develop type-off="Дизайн" back="/image/main/caseOne.webp" title="UI/UX сайтов" date="до 15 дней" description="Сайты-визитки для приема заявок"/>
      <develop type-off="Дизайн" back="/image/main/caseTwo.webp" title="UI/UX приложений" date="от 30 дней" description="сложный интрнет-магазин с подключением онлайн-касс и собственной админ панелью"/>
      <develop type-off="Дизайн" back="/image/main/caseThree.webp" title="Дизайн Logo" date="до 30 дней" description="Многостраничный сайт с собственной админ панелью"/>
    </div>
  </div>
</template>

<style scoped lang="scss">
.develop{
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
</style>