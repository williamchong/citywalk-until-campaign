<template>
  <UButton
    size="xl"
    variant="soft"
    @click="onClickPurchase"
    target="_blank"
    to="https://liker.land/zh-Hant/nft/class/likenft1rvwlaaedlfewy0h4cyrfduc5xcgxh740wpavvzj885hmmjxpwzwscavef3?channel=liker_land&utm_source=purchase_button&utm_medium=web&utm_campaign=citywalk_until"
  >購買《城市散步學》</UButton>
</template>

<script setup lang="ts">
const props = defineProps({
  from: {
    type: String,
    default: '',
  }
})

function onClickPurchase() {
  useTrackEvent(`clickPurchaseButton${props.from || ''}`)
}
</script>
