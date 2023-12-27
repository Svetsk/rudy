<script setup>
defineProps({
  back: String,
  title: String,
  date: String,
  description: String,
  pageSrc: String,
  typeOff: String,
})
</script>
<template>
<div class="dev__item" >
  <div class="flex items-center gap-[16px]">
    <nuxt-img class="logo" src="image/logo.jpg" width="42px" />
    <p class="size-[32]">{{ typeOff }}</p>
  </div>
  <div class="flex flex-col gap-[48px]">
    <div>
      <p>{{ title }}</p>
      <p>Срок: {{ date }}</p>
    </div>
    <p class="desc">{{ description }}</p>
  </div>
  <nuxt-link :to="pageSrc">Заказать ></nuxt-link>
  <nuxt-img class="imagess" :src="back" width="200px" />
</div>
</template>

<style scoped lang="scss">
.dev__item{
  flex: 49%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  row-gap: 20px;
  background: rgba(52, 52, 52, 0.44);
  padding: 40px 80px;
  border-radius: 20px;
  position: relative;
  & .imagess{
    transition: 0.5s;
  }
  &:hover .imagess{
    transform: translateY(-10px);
  }
  & p:nth-child(1){
    font-size: 32px;
    color: #2CB67D;
    font-weight: 900;
  }
  & div > p:nth-child(2){
  }
  & .logo{
    border-radius: 100px;
  }
  & a{
    margin-top: 64px;
  }
}
.desc{
  max-width: 420px;
}
.imagess{
  position: absolute;
  bottom: 30px;
  right: 0;
}
</style>