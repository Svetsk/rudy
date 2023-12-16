<template>
    <div>
        <div class="stats">
            <img :src="imgSrc" alt="">
            <p class="title__stats">{{ title }}</p>
            <p>{{ subtitle }}</p>
        </div>
    </div>
</template>

<script setup>
defineProps({
    title: String,
    subtitle: String,
    imgSrc: {
        type: String,
        default: "carbon:play-filled",
    },
});
</script>

<style lang="scss" scoped>
  .title__stats{
      color: #000;
      font-family: 'Museo Sans Cyrl';
      font-size: 24px;
      font-weight: 400;
      line-height: 109.8%; /* 26.352px */
  }
</style>