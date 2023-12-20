<script setup lang="ts">
const popap = usePopap();

useSeoMeta({
  title: "Rudy Studio",
  ogTitle: "Rudy Studio",
});
</script>

<template>
  <div class="main">
    <MainModalPop v-if="popap.buttonTrigger">
      <MainCountForm />
    </MainModalPop>
    <MainModalPop v-if="popap.timerTrigger">
      <div class="success">
        <h3>Заявка отправлена</h3>

        <button class="calc" @click="() => (popap.timerTrigger = !popap.timerTrigger)">Ok</button>
      </div>
    </MainModalPop>
    <MainOffer />

    <MainOnlineMessage />
    <MainCostDev />
    <MainSocial />
    <MainStep />
    <MainWorks />
    <MainRequ />
    <MainCostSeo />
    <MainDescription />
    <MainModal id="count" />
  </div>
</template>

<style lang="scss" scoped>
.success {
  background: #fff;
  padding: 50px;
  display: grid;
  row-gap: 20px;

  & button {
    display: grid;
    place-content: center;
  }
}
</style>
