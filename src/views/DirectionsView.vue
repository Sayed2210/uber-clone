<template>
  <div class="directions">
    <div class="grid grid-cols-12 mt-4 shadow-md">
      <div class="col-span-2 mx-auto">
        <div @click="router.push('/')">
          <ArrowLeftIcon :size="35" />
        </div>
        <div class="h-16 mt-4 w-full">
          <div :class="[isPickupActive ? 'circle-black' : 'circle-gray']" />
          <div class="line"></div>
          <div :class="[!isPickupActive ? 'square-black' : 'square-gray']" />
        </div>
      </div>
      <div class="col-span-10">
        <AutoCompleteInput />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import ArrowLeftIcon from "vue-material-design-icons/ArrowLeft.vue";
import { useRouter } from "vue-router";
import AutoCompleteInput from "@/components/AutoCompleteInput.vue";
const router = useRouter();

const isPickupActive = ref(false);
</script>

<style lang="scss" scoped>
.directions {
  height: 100vh;
  .bg-custom-color {
    background-color: rgb(237, 237, 237);
  }

  .circle-black {
    margin: 0 auto;
    width: 9px;
    height: 9px;
    background-color: black;
    border-radius: 100%;
  }

  .circle-gray {
    margin: 0 auto;
    width: 9px;
    height: 9px;
    background-color: rgb(191, 191, 191);
    border-radius: 100%;
  }

  .square-black {
    margin: 0 auto;
    width: 9px;
    height: 9px;
    background-color: black;
  }

  .square-gray {
    margin: 0 auto;
    width: 9px;
    height: 9px;
    background-color: rgb(191, 191, 191);
  }

  .line {
    margin: 0 auto;
    width: 2px;
    height: 45px;
    background-color: rgb(191, 191, 191);
  }

  .custom-border-bottom {
    border-bottom: 1px solid rgb(230, 230, 230);
  }
}
</style>
