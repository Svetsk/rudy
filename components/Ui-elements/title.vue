<script setup lang="ts">
defineProps({
  title: String,
  subTitle: String,
})
</script>

<template>
  <div class="title">
    <p>{{ title }} <span>{{ subTitle }}</span></p>
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
</style>