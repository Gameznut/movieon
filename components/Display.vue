<!-- Please remove this file from your project -->
<template>
  <div>
    <LargeDisplay />
    <!-- Now playing -->
    <div class="">
      <h1 class="text-gray-500 py-6 font-bold text-2xl">Now Playing</h1>
      <div class="card overflow-x-scroll">
        <Card
          class=""
          :now_playing="nowplaying"
          v-for="(nowplaying, i) in nowplaying.results"
          :key="i"
        />
      </div>
    </div>

    <!-- trending -->
   <div class="">
      <h1 class="text-gray-500 py-6 font-bold text-2xl">Trending</h1>
      <div class="card overflow-x-scroll">
        <Card2
          class=""
          :trends="trend"
          v-for="(trend, i) in trending.results"
          :key="i"
        />
      </div>
    </div> 
    <!-- Popular tv show -->
       <div class="">
      <h1 class="text-gray-500 py-6 font-bold text-2xl">Popular Shows</h1>
      <div class="card overflow-x-scroll">
        <Card3
          class=""
          :popular="popular"
          v-for="(popular, i) in popular.results"
          :key="i"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NuxtTutorial",
  data() {
    return {
      nowplaying: [],
      trending: [],
      popular: []
    };
  },
  async fetch() {
    this.nowplaying = await fetch(
      `https://api.themoviedb.org/3/movie/now_playing?api_key=${process.env.APIKEY}`
    ).then((res) => res.json());
    this.trending = await fetch(
      `https://api.themoviedb.org/3/trending/all/day?api_key=${process.env.APIKEY}`
    ).then((res) => res.json());
    this.popular = await fetch(
      `https://api.themoviedb.org/3/tv/popular?api_key=${process.env.APIKEY}`
    ).then((res) => res.json());
  },
};
</script>
<style scoped>
.card {
  display: flex;
  /* flex-wrap: wrap; */
  gap: 20.7px;
}
</style>