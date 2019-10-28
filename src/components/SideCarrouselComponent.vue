<template>
  <div class="flex text-gray-900">
    <div class="_bg-gray-500 w-full lg:w-2/3">
      <div class="relative pb-2/3 overflow-hidden rounded-l-lg shadow-lg">
        <img
          class="absolute w-full h-full object-cover object-bottom"
          :src="images[currentIndex].imageUrl"
        />
        <!-- Buttons -->
        <span class="block sm:hidden">
          <svg
            class="absolute w-10 h-10 ml-4 icon fill-current text-gray-100 hover:text-indigo-500"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
          >
            <path
              d="M10 20a10 10 0 1 1 0-20 10 10 0 0 1 0 20zm8-10a8 8 0 1 0-16 0 8 8 0 0 0 16 0zM7.46 9.3L11 5.75l1.41 1.41L9.6 10l2.82 2.83L11 14.24 6.76 10l.7-.7z"
            />
          </svg>
          <svg
            class="absolute w-10 h-10 mr-4 right-0 icon fill-current text-gray-100 hover:text-indigo-500"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
          >
            <path
              d="M10 0a10 10 0 1 1 0 20 10 10 0 0 1 0-20zM2 10a8 8 0 1 0 16 0 8 8 0 0 0-16 0zm10.54.7L9 14.25l-1.41-1.41L10.4 10 7.6 7.17 9 5.76 13.24 10l-.7.7z"
            />
          </svg>
        </span>
      </div>
    </div>
    <!-- Side -->
    <div class="hidden lg:flex w-1/3">
      <div class="flex flex-col justify-between w-full overflow-hidden rounded-r-lg shadow-lg">
        <div
          :class="currentIndex == i ? 'bg-gray-800' : 'bg-gray-900'"
          class="h-full border-gray-200 p-4 hover:bg-gray-700 hover-rooms transition-all"
          v-for="(image, i) in images"
          :key="image.imageUrl"
        >
          <a href="#" @click.prevent="showImage(i)">
            <h4
              class="text-md sm:text-lg text-gray-400 font-semibold leading-tight truncate mt-1"
            >{{ image.title }}</h4>
            <div class="mt-1 text-gray-500">
              {{ image.formattedPrice }}
              <span
                class="text-gray-600 text-sm"
              >&bullet; {{image.beds}} Habitaciones</span>
            </div>
            <div class="mt-4 text-orange-500">L'Hort de Senabre, València</div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: ["images"],
  data() {
    return {
      currentIndex: 0
    };
  },
  methods: {
    showImage(imageIndex) {
      this.currentIndex = imageIndex;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.pb-2\/3 {
  padding-bottom: 66%;
}

.icon {
  top: calc(50% - 2.5rem / 2);
}



.transition-all {
  transition: all 0.3s ease;
}
</style>
