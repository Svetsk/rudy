<script setup lang="ts">
defineProps({
  title: String,
  subTitle: String,
  podtitle: String,
  labelOne: String,
  labelTwo: String,
  labelThree: String,
})
</script>

<template>
  <div class="title">
    <p>{{ title }} <span>{{ subTitle }}</span></p>
    <p class="podtitle">{{ podtitle }}</p>
    <div class="flex gap-1">
      <p class="label">{{ labelOne }}</p>
      <p class="label">{{ labelTwo }}</p>
      <p class="label">{{ labelThree }}</p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.title{
  padding: 90px 0 20px 0;
}
p{
  font-size: 64px;
  font-weight: 900;
}
span{
  color: #2CB67D;
}
.label {
  background: #343434;
  color: #ffffff;
  padding: 4px 8px;
  font-size: 18px;
  font-weight: 200;
  border-radius: 6px;
  display: inline-block;
}
.podtitle{
  font-size: 24px;
  font-weight: 400;
  max-width: 720px;
  padding: 20px 0 40px 0;
}
.gap-1{
  padding-bottom: 40px;
}
</style>