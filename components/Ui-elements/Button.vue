<script setup>
defineProps({
  title: {
    type: String,
    default: "Расчитать стоимость",
  },
  btnSlot: Boolean,
});
</script>

<template>
  <div class="button">
    <button v-if="!btnSlot">{{ title }}</button>
    <button v-else><slot /></button>
  </div>
</template>

<style scoped lang="scss">
.button button {
  color: #1536df;
  font-family: "Inter";
  font-size: 16px;
  font-weight: 700;
  padding: 17px 100px;
  border: 1px solid #1536df;
  border-radius: 5px;
  background: none;
  margin: 0 40px 30px 40px;

  &:hover {
    background: #1536df;
    color: #fff;
  }
}
</style>
