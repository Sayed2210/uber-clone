<template>
  <div class="service-select-small">
    <div class="w-full rounded-2xl bg-custom flex justify-center items-center">
      <div class="flex justify-center items-center">
        <!-- :src="`@/assets/img/uber/${img}.png`" -->
        <img :src="'img/uber/' + img + '.png'" class="w-16" alt="" />
      </div>
    </div>
    <div class="text-lg text-center text-gray-900">{{ text }}</div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  img: String,
  text: String,
});
</script>

<style scoped lang="scss">
.service-select-small {
  > div {
    height: 70px;
  }
  .bg-custom {
    background-color: rgb(237, 237, 237);
  }
}
</style>
