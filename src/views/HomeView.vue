<template>
  <div class="home flex flex-col h-screen">
    <div class="my-20 mx-auto">
      <img width="150" src="img/uber/uber2.svg" />
    </div>
    <div class="grid grid-cols-2 gap-3 my-3">
      <ServiceSelect img="ride" text="Ride" imageWidth="120" />
      <ServiceSelect img="food" text="Food" imageWidth="120" :promo="true" />
    </div>
    <div class="grid grid-cols-4 gap-2 my-3">
      <ServiceSelectSmall img="travel" text="Travel" />
      <ServiceSelectSmall img="2wheels" text="2 Wheels" />
      <ServiceSelectSmall img="transit" text="Transit" />
      <ServiceSelectSmall img="reserve" text="Reserve" />
    </div>
    <div class="w-full bg-custom h-14 rounded-full flex items-center p-3">
      <MagnifyIcon :size="30" fillColor="#1f1e1e" />
      <div class="ml-3 text-xs font-semibold text-gray-700">
        Enter pick-up point
      </div>
    </div>
    <footer
      class="w-full z-50 flex justify-around p-1 fixed bottom-0 mb-2 border-t-2 border-t-gray-200"
    >
      <div class="grid place-items-center">
        <HomeIcon :size="30" fillColor="#1f1e1e" />
        <div
          class="w-full -mt-1 text-xs text-center text-gray-800 font-semibold"
        >
          Home
        </div>
      </div>
      <div class="grid place-items-center">
        <MapMarkerIcon :size="30" fillColor="#b3b1b1" />
        <div
          class="w-full -mt-1 text-xs text-center text-gray-400 font-semibold"
        >
          Destination
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import ServiceSelect from "@/components/ServiceSelect.vue";
import ServiceSelectSmall from "@/components/ServicesSelectSmall.vue";
import MagnifyIcon from "vue-material-design-icons/Magnify.vue";
import HomeIcon from "vue-material-design-icons/Home.vue";
import MapMarkerIcon from "vue-material-design-icons/MapMarker.vue";
</script>

<style lang="scss">
.bg-custom {
  background-color: rgb(237, 237, 237);
}
</style>
