<!-- Please remove this file from your project -->
<template>
  <div>
    <LargeDisplay />
    <div >
      <h1 class="text-gray-500 py-6 font-bold text-2xl">Now Playing</h1>
      <div class="flex gap-5">
        <Card v-for="i in 5" :key="i" />
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: "NuxtTutorial",
};
</script>
