<script setup lang="ts">
defineProps({
  imgSrc: {
    type: String,
    default: "image/main/caseOne.webp",
  },
  title: String,
  description: String,
  labelOne: String,
  labelTwo: String,
  labelThree: String,
  labelFour: String,
})
</script>

<template>
  <div class="servises__block">
    <div>
      <nuxt-img :src="imgSrc" />
    </div>
    <div>
      <strong>{{ title }}</strong>
      <p>{{ description }}</p>
    </div>
    <div>
      <p>{{ labelOne }}</p>
      <p>{{ labelTwo }}</p>
      <p>{{ labelThree }}</p>
      <p>{{ labelFour }}</p>
    </div>
    <div>
      <p class="more">Подробнее ></p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.servises__block {
  background: rgba(24, 24, 24, 0.76);
  border-radius: 20px;
  padding: 40px 60px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  transition: 1s;
  & *{
    transition: 0.5s;
  }
  &:hover {
    background: #343434;
    & img {
      transform: translateY(-10px);
    }
  }
  & div:nth-child(2) strong {
    font-size: 32px;
  }

  & div:nth-child(2) p {
    max-width: 230px;
  }

    & div:nth-child(3) {
      display: flex;
      flex-wrap: wrap;
      row-gap: 4px;
      column-gap: 12px;
      & p {
        background: black;
        color: #b6b6b6;
        padding: 4px 8px;
        border-radius: 6px;
      }
    }
}
.more:hover{
  text-decoration: underline;
}
</style>