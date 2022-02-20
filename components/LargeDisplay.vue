<template>
  <div class="thumbnail w-full bg-orange-600">
    <div class="pl-20 absolute top-36">
      <p class="uppercase font-semibold text-gray-400 pb-6">
        {{ movies.currentSeason }}
      </p>
      <h1 class="font-bold text-6xl uppercase text-slate-200">
        {{ movies.title }}
      </h1>
      <div class="flex pt-5 gap-1 uppercase font-semibold">
        <span
          class="text-gray-300"
          v-for="(genre, id) in movies.category"
          :key="id"
          >{{ genre }}</span
        >
      </div>
      <div class="flex gap-3 pt-10">
        <button class="bg-red-400 text-white px-14 py-3">Watch Now</button>
        <button class="bg-gray-400 font-bold text-3xl text-white px-9 py-3">
          +
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      movies: {
        title: "Supernatural",
        category: ["Action, ", "Horror, ", "Comedy"],
        currentSeason: "Season 10",
      },
    };
  },
};
</script>

<style scoped>
.thumbnail{
    height: 500px;
    background-image: url('../assets/img/supernatural.jpg');
    background-repeat: no-repeat;
    /* background-position: contain; */
    background-size: 100%;
}
</style>