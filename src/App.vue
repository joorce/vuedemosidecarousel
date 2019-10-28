<template>
  <div id="app">
    <SideCarrouselComponent :images="data" class="max-w-full sm:max-w-4xl m-auto p-4"></SideCarrouselComponent>
  </div>
</template>

<script>
import SideCarrouselComponent from "./components/SideCarrouselComponent.vue";
export default {
  name: "app",
  components: { SideCarrouselComponent },
  data() {
    return {
      data: [
        {
          imageUrl: "https://source.unsplash.com/KJFKCed0YKo/1600x900",
          imageAlt: "Rear view of modern home with pool",
          beds: 3,
          baths: 2,
          title: "Fantástico",
          priceInCents: 190000,
          formattedPrice: "$1,900.00",
          reviewCount: 34,
          rating: 4
        },
        {
          imageUrl: "https://source.unsplash.com/tHkJAMcO3QE/1600x900",
          imageAlt: "Rear view of modern home with pool",
          beds: 3,
          baths: 2,
          title: "Adosado en Gaspar Aguilar",
          priceInCents: 357000 ,
          formattedPrice: "357.000 €",
          reviewCount: 34,
          rating: 4
        },
        {
          imageUrl: "https://source.unsplash.com/BZdv_I1LeLg/1600x900",
          imageAlt: "Rear view of modern home with pool",
          beds: 3,
          baths: 2,
          title: "Piso en Na Rovella",
          priceInCents: 190000,
          formattedPrice: "$1,900.00",
          reviewCount: 34,
          rating: 4
        }
      ]
    };
  }
};
</script>

<style src="./assets/tailwind.css">
