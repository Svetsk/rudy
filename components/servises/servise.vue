<script setup lang="ts">

</script>

<template>
  <div>
    <ui-elements-title title="Услуги нашего" sub-title="агентства" />
  <div class="servises">
    <nuxt-link to="/servises/development">
      <ui-elements-servises-block
          img-src="image/main/caseOne.webp"
          title="Разработка"
          description="Для малого, среднего бизнеса - разработка сайта под ключ"
          label-one="малый бизнес"
          label-two="средний бизнес"
          label-four="собственники со своей командой"
          label-three="эксперты" />
    </nuxt-link>
    <nuxt-link to="/servises/marketing">
      <ui-elements-servises-block
          img-src="image/main/caseTwo.webp"
          title="Продвижение"
          description="Для малого, среднего бизнеса - разработка сайта под ключ"
          label-one="малый бизнес"
          label-two="средний бизнес"
          label-three="собственники со своей командой"
          label-four="эксперты" />
    </nuxt-link>
    <nuxt-link to="/servises/seo">
      <ui-elements-servises-block
          img-src="image/main/caseThree.webp"
          title="Дизайн"
          description="Для малого, среднего бизнеса - разработка сайта под ключ"
          label-one="малый бизнес"
          label-two="средний бизнес"
          label-three="собственники со своей командой"
          label-four="эксперты" />
    </nuxt-link>
  </div>
  </div>
</template>

<style scoped lang="scss">
.servises{
  display: flex;
  justify-content: space-between;
  gap: 20px;
}
</style>