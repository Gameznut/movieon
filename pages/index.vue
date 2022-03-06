<template>
  <div class="flex relative bg-black">
    <Nav class="fixed" />
    <Display class="w-9/12 ml-56 px-12 border-l border-r border-gray-400" />
    <Nav class="w-96 fixed navright" />
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>
<style scoped>
.navright{
  right: -131px;
}
</style>
