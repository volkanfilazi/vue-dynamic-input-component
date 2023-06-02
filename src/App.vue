<script setup lang="ts">
import { ref } from 'vue';
import VInput from './components/V-Input.vue'
const firstName = ref<string>('')
const lastName = ref<string>('')
const phone = ref<string>('')


</script>

<template>
  <div class="flex flex-col items-center gap-2 w-full h-screen justify-center bg-black">
    <h2 class="text-yellow-400">Input some values you will see the changes</h2>
      <VInput place-value="firstname" type-value="string" v-if="firstName !== undefined" v-model="firstName"></VInput>
      <VInput id="lastname" place-value="lastname" type-value="string" v-model="lastName"></VInput>
      <VInput id="phone" place-value="phone" type-value="number" v-model="phone"></VInput>
      <VolkiButton>asdas</VolkiButton>
    <div class="text-white">
      <p v-if="firstName">firstname: {{ firstName }}</p>
      <p v-if="lastName">lastname: {{ lastName }}</p>
      <p v-if="phone">phone: {{ phone }}</p>
    </div>
  </div>
</template>

<style scoped></style>
