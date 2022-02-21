<template>
  <div class="container bg-gray-300">
    <div class=" w-full">
      <div
        :style="{
          backgroundImage: `url(https://image.tmdb.org/t/p/w300/${popular.poster_path})`,
        }"
        class="thumbnail relative px-4"
      >
        <button
          class="
            text-center
            p-2
            px-3
            hover:bg-gray-400
            font-bold
            text-4xl text-white
            bg-gray-800 bg-opacity-90
            mt-4
            float-right
            mb-40
          "
        >
          <span class="flex items-center justify-center">
            <svg
              version="1.1"
              id="Layer_1"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              x="0px"
              y="0px"
              viewBox="0 0 455 455"
              style="enable-background: new 0 0 455 455"
              xml:space="preserve"
              width="25"
              fill="white"
            >
              <polygon
                points="455,212.5 242.5,212.5 242.5,0 212.5,0 212.5,212.5 0,212.5 0,242.5 212.5,242.5 212.5,455 242.5,455 242.5,242.5 455,242.5 "
                style="fill: white; stroke: white; stroke-width: 50"
              />
            </svg>
          </span>
        </button>
        <button
          class="
            bg-red-500
            show
            absolute
            bottom-0
            right-0
            text-center
            py-4
            w-full
          "
        >
          Watch Now
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["popular"],
};
</script>

<style scoped>
.thumbnail {
  background-position: cover;
  background-repeat: no-repeat;
  background-size: 100%;
  width: 300px;
  height: 440px;
}
.show {
  display: none;
}
.show:hover {
  display: block;
}
.container {
  width: 400px;
}
</style>