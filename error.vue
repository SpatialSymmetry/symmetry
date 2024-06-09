

<template>

  <div class="w-full min-h-screen bg-black">


  <div class="max-w-screen-lg mx-auto text-center p-4 pt-24">
    <p class="font-extrabold tracking-tight text-gray-200 text-5xl mb-16">{{ error.statusCode }}</p>
    <p class="font-extrabold tracking-tight text-gray-200 text-3xl">We're Currently Under Development.</p>
    <div class="mt-4 mb-8 sm:px-16 xl:px-48 text-gray-400"><button @click="handleError">Go to the home page</button></div>
  </div>

  </div>

</template>


<script setup>
const props = defineProps({
  error: Object,
  required: true,
});

const handleError = () => clearError({ redirect: '/' });
</script>

