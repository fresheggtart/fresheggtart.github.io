<template>
  <div
    id="app"
    class="min-h-screen xl:h-screen antialiased bg-gray-200 xl:flex xl:flex-col"
  >
    <SiteHeader class="" />

    <div class="xl:flex-1 xl:flex xl:overflow-y-hidden">
      <SearchFilter />
      <main class="px-4 py-6">
        <h3 class="text-xl text-gray-900">Los Angeles</h3>
        <p class="text-gray-600">
          Live like the stars in the ipsum dolor sit amet, consectetur
          adipiscing elit, sed do eiusmod tempor incididunt
        </p>
        <div class="mt-6 flex flex-wrap sm:-mx-2 sm:overflow-x-auto sm:pb-8 ">
          <div v-for="(property, i) in properties" >
            <PropertyCard :property="property" />
          </div>
        </div>
      </main>
    </div>
  </div>
</template>
<script>
import SiteHeader from "@/components/SiteHeader.vue";
import SearchFilter from "@/components/SearchFilter.vue";
import PropertyCard from "@/components/PropertyCard";

export default {
  name: "app",
  components: {
    SiteHeader,
    SearchFilter,
    PropertyCard,
  },
  data() {
    return {
      properties: [
        {
          imageUrl:
            "https://images.unsplash.com/photo-1580587771525-78b9dba3b914?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 2,
          baths: 2,
          title: "Modern home in city center",
          price: "14000",
          reviewCount: 34,
          rating: 4,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1564501049412-61c2a3083791?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 4,
          baths: 2,
          title: "Modern home in city center",
          price: "20000",
          reviewCount: 35,
          rating: 4,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1531971589569-0d9370cbe1e5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 2,
          baths: 3,
          title: "Modern home in city center",
          price: "100",
          reviewCount: 2,
          rating: 3,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1564013799919-ab600027ffc6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 4,
          baths: 3,
          title: "Modern home in city center",
          price: "53320",
          reviewCount: 314,
          rating: 1,
        },
      ],
    };
  },
};
</script>
<style src="./assets/css/tailwind.css"></style>
