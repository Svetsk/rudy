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
      <h3>Pop Time</h3>
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
    <MainModal />
  </div>
</template>
