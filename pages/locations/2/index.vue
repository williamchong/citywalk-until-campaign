<template>
  <div>

    <header class="p-8 bg-[#ABAB8A] text-center text-white">
      <h1 class="flex justify-between tracking-widest">
        <span class="text-2xl font-cursive">地點 2</span><span class="text-3xl font-bold font-serif">路徑</span>
      </h1>
    </header>

    <main class="flex flex-col justify-center items-center text-left grow gap-4 p-8 pb-0">
      <img class="rounded-2xl w-full max-w-[40vh]" src="~assets/images/location-2.jpg" />
  
      <div class="text-center">
        <div class="font-bold text-lg">通道</div>
        <div>步行距離約 5 分鐘</div>
      </div>

      <UButton
        @click="onClickMap"
        size="xl"
        variant="outline"
        color="black"
        target="_blank"
        rel="noopener"
        to="https://www.google.com/maps/dir/Until+coffee,+%E9%91%BD%E7%9F%B3%E5%B1%B1/%E7%AB%B9%E5%9C%92%E5%BD%A9%E8%99%B9%E9%81%93150%E8%99%9F%E5%BD%A9%E8%99%B9%E9%81%93%E9%AB%94%E8%82%B2%E9%A4%A8/@22.3372362,114.1962751,19z/data=!4m14!4m13!1m5!1m1!1s0x3404075cb192b285:0xe5753b37e7c71d12!2m2!1d114.1981629!2d22.338325!1m5!1m1!1s0x340406d746941b23:0x5b9cfa0ea6db16fd!2m2!1d114.196468!2d22.337071!3e2?entry=ttu"
      >
        打開地圖
      </UButton>
    </main>

    <footer class="flex justify-center p-8">
      <UButton @click="onClickArrive" size="xl" :to="{ name: 'locations-2-description' }">我到了</UButton>
    </footer>

  </div>
</template>

<script setup lang="ts">
function onClickMap() {
  useTrackEvent('OpenMapLocation2')
}

function onClickArrive() {
  useTrackEvent('ArriveLocation2')
}
</script>
