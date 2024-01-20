<template>
  <div class="auto-complate">
    <div class="flex items-center">
      <input
        :id="theId"
        type="text"
        class="text-md bg-gray-100 appearance-none rounded w-full py-2.5 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:bg-gray-200"
        :placeholder="placeholder"
        v-model="inputComplate"
        @click="emit('isActive', true)"
      />
      <WindowCloseIcon class="ml-2" @click="emit('clearInput')" />
    </div>
  </div>
</template>
<script setup>
import { defineProps, defineEmits } from "vue";
import WindowCloseIcon from "vue-material-design-icons/WindowClose.vue";

defineProps({
  theId: String,
  input: String,
  placeholder: String,
});
const emit = defineEmits(["isActive", "clearInput"]);
</script>
<style scoped></style>
