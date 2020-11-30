<template>
  <div class="sm:max-w-xs sm:w-full sm:flex-shrink-0 pl-10 sm:mt-10 mt-10">
    <div class="relative pb-5/6">
      <img
        class="absolute inset-0 h-full object-cover w-screenx rounded-lg shadow-md"
        :src="property.imageUrl"
      />
    </div>
    <!--relative allows you to negative margin and pop up in front-->
    <div class="relative px-4 -mt-16">
      <div class="px-4 py-4 bg-white rounded-lg shadow-lg">
        <div class="flex">
          <span
            class="inline-block px-2 py-1 text-xs font-semibold leading-none tracking-wide text-teal-800 uppercase bg-teal-200 rounded-full"
            >Plus</span
          >
          <div
            class="ml-2 text-xs font-semibold tracking-wide text-gray-600 uppercase"
          >
            {{ property.beds }}
            {{ property.beds === 1 ? "bed" : "beds" }} &bull;
            {{ property.baths }} {{ property.bath === 1 ? "bath" : "baths" }}
          </div>
        </div>
        <div class="mt-1">
          <h3 class="text-lg font-semibold text-gray-900">
            {{ property.title }}
          </h3>
        </div>
        <div class="mt-1">
          <span class="text-gray-900">{{ formattedPrice }}</span>
          <span class="ml-1 text-sm text-gray-600">/wk</span>
        </div>
        <div class="flex items-center mt-2 text-sm text-gray-600 ">
          <svg
            v-for="i in 5"
            class="w-4 h-4 fill-current"
            :class="property.rating >= i ? 'text-teal-500' : 'text-gray-400'"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 478.53 478.53"
          >
            <path
              d="M477.795 184.279a14.997 14.997 0 00-12.108-10.209l-147.159-21.384-65.812-133.35a15 15 0 00-26.902 0l-65.812 133.35L12.843 174.07A14.996 14.996 0 00.735 184.279a14.997 14.997 0 003.796 15.376l106.484 103.798-25.138 146.565a15.002 15.002 0 0021.765 15.813l131.623-69.199 131.623 69.199a14.998 14.998 0 0015.797-1.141 15.002 15.002 0 005.968-14.671l-25.138-146.565 106.484-103.798a15 15 0 003.796-15.377z"
            />
          </svg>

          {{ property.reviewCount }}
          {{ property.reviewCount === 1 ? "review" : "reviews" }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["property"],
  data() {
    return {};
  },
  methods: {},
  computed: {
    formattedPrice() {
      const formatter = new Intl.NumberFormat("en-US", {
        style: "currency",
        currency: "USD",
      });
      return formatter.format(this.property.price / 100);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>

