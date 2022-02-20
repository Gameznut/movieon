<template>
  <div>
    <nav class="py-2 w-60">
      <div class="pt-4 pl-10">MovieOn</div>
      <div class="">
        <!-- menu -->
        <div>
          <h1 class="py-3 text-gray-400 font-bold">Menu</h1>
          <div v-for="(menu, id) in menus" :key="id">
            <p class="py-2 text-gray-500 font-bold">
              <span></span>{{ menu.title }}
            </p>
          </div>
        </div>
        <!-- library -->
        <div class="py-4">
          <h1 class="py-3 text-gray-400 font-bold">Library</h1>
          <div v-for="(menu, id) in libraries" :key="id">
            <p class="py-2 text-gray-500 font-bold">
              <span></span>{{ menu.title }}
            </p>
          </div>
        </div>
        <!-- category -->
        <div class="py-4">
          <h1 class="py-3 text-gray-400 font-bold">Category</h1>
          <div v-for="(menu, id) in categories" :key="id">
            <p class="py-2 text-gray-500 font-bold">
              <span></span>{{ menu.title }}
            </p>
          </div>
        </div>
        <!-- General -->
        <div class="py-4">
          <h1 class="py-3 text-gray-400 font-bold">General</h1>
          <div v-for="(menu, id) in general" :key="id">
            <p class="py-2 text-gray-500 font-bold">
              <span></span>{{ menu.title }}
            </p>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menus: [
        {
          title: "Home",
          icon: "",
          to: "/",
        },
        {
          title: "Communtiy",
          icon: "",
          to: "/",
        },
        {
          title: "Discover",
          icon: "",
          to: "/",
        },
        {
          title: "Awards",
          icon: "",
          to: "/",
        },
        {
          title: "Celebs",
          icon: "",
          to: "/",
        },
      ],
      libraries: [
        {
          title: "Recent",
          icon: "",
          to: "/",
        },
        {
          title: "Top Rated",
          icon: "",
          to: "/",
        },
        {
          title: "Dowloaded",
          icon: "",
          to: "/",
        },
      ],
      categories: [
        {
          title: "TV - Show",
          icon: "",
          to: "/",
        },
        {
          title: "Movie",
          icon: "",
          to: "/",
        },
        {
          title: "Anime",
          icon: "",
          to: "/",
        },
      ],
      general: [
        {
          title: "Settings",
          icon: "",
          to: "/",
        },
        {
          title: "Log Out",
          icon: "",
          to: "/",
        },
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  padding-left: 2.5rem /* 40px */;
}
p {
  padding-left: 2.5rem /* 40px */;
}
P:hover {
  cursor: pointer;
  background-color: rgb(54, 204, 241);
}
</style>