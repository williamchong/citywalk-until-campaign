<template>
  <div>

    <header class="p-8 bg-[#ABAB8A] text-center text-white">
      <h1 class="flex justify-between tracking-widest">
        <span class="text-2xl font-cursive">地點 3</span><span class="text-3xl font-bold font-serif">空間</span>
      </h1>
    </header>

    <main class="flex flex-col justify-center items-center text-left grow gap-4 p-8 pb-0">
      <img class="rounded-2xl w-full max-w-[40vh]" src="~assets/images/location-3.jpg" />

      <div class="text-center">
        <div class="font-bold text-lg">遊樂場</div>
        <div>步行距離約 5 分鐘</div>
      </div>

      <UButton
        @click="onClickMap"
        size="xl"
        variant="outline"
        color="black"
        target="_blank"
        rel="noopener"
        to="https://www.google.com/maps/dir/Until+coffee,+%E9%91%BD%E7%9F%B3%E5%B1%B1/%E6%96%B0%E8%92%B2%E5%B4%97%E5%B4%87%E9%BD%A1%E8%A1%97%E5%B4%87%E9%BD%A1%E8%A1%97%E9%81%8A%E6%A8%82%E5%A0%B4/@22.3355745,114.1964057,17z/data=!4m14!4m13!1m5!1m1!1s0x3404075cb192b285:0xe5753b37e7c71d12!2m2!1d114.1981629!2d22.338325!1m5!1m1!1s0x340406d7204ef985:0x9f893d74ded46ecc!2m2!1d114.1964057!2d22.3355745!3e2?entry=ttu"
      >
        打開地圖
      </UButton>
    </main>

    <footer class="flex justify-center p-8">
      <UButton @click="onClickArrive" size="xl" :to="{ name: 'locations-3-description' }">我到了</UButton>
    </footer>

  </div>
</template>

<script setup lang="ts">
function onClickMap() {
  useTrackEvent('OpenMapLocation3')
}

function onClickArrive() {
  useTrackEvent('ArriveLocation3')
}
</script>
