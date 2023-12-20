<script setup lang="ts">
import { useArticleStore } from "@/stores/postStore";
import { usePriceStore } from "@/stores/priceStore";
import { storeToRefs } from "pinia";

const { postList } = storeToRefs(useArticleStore());
const { getPostList } = useArticleStore();

const { priceList } = storeToRefs(usePriceStore());
const { getPriceList } = usePriceStore();

const loadStores = async () => {
  if (!postList.value?.length) {
    await getPostList();
  }
  if (!priceList.value?.length) {
    await getPriceList();
    console.log(priceList.value);
  }
};
//Load all stores

await loadStores();
</script>

<template>
  <div class="default">
    <UiAddHeader />
    <main>
      <slot />
    </main>
    <UiAddFooter />
  </div>
</template>
