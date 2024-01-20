<template>
  <div class="service-select">
    <div class="w-full rounded-2xl bg-custom">
      <div v-if="promo" class="w-full relative z-10">
        <span
          class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 bg-green-700 p-0.5 px-2 text-gray-100 rounded-3xl text-xs"
        >
          Promo
        </span>
      </div>
      <div class="flex justify-between">
        <div class="text-lg ml-3 mt-16 text-gray-900">{{ text }}</div>
        <div class="mt-3 ml-1">
          <!-- :src="`@/assets/img/uber/${img}.png`" -->
          <img
            :src="'img/uber/' + img + '.png'"
            :width="imageWidth"
            class="max-w-full"
            alt=""
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  img: String,
  text: String,
  imageWidth: String,
  promo: { Boolean, default: false },
});
</script>

<style scoped lang="scss">
.service-select {
  > div {
    height: 100px;
  }
  .bg-custom {
    background-color: rgb(237, 237, 237);
  }
}
</style>
