<template>
  <section class="bg-gray-800 xl:w-72">
    <div class="flex justify-between px-4 py-3 xl:hidden">
      <div class="relative max-w-sm w-full">
        <div
          class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
        >
          <svg
            class="w-6 h-6 text-gray-600 fill-current"
            version="1.0"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 1244 1280"
          >
            <path
              d="M402.5 1.1C299.6 9 205.6 51.2 132.1 122.5 33.6 218-13.5 351.7 3.6 487.5c15.6 124.4 84.9 236 189.9 305.9 19.3 12.9 27.2 17.5 47 27.4 45.2 22.7 90.6 36.2 144.5 42.9 20.7 2.5 76.3 2.5 97 0 40.4-5 75.2-13.8 111.5-28.1 25.1-9.8 60-28.3 81.9-43.3l8-5.4 107.5 107.3c383.5 382.7 377 376.2 382.8 379.5 18.9 10.5 41.1 7.5 56.3-7.7 14.8-14.8 18-35.9 8.4-55.3-2.1-4.3-46.2-48.8-243.2-245.9C774 743.5 754.8 724 756 722.3c.8-1 4-4.7 7-8.3 71.4-83.6 108.8-192.7 103.1-301.1-3.2-61-16.5-113.6-42-166.4-16.9-34.9-34-61.5-59.2-92-10.6-12.8-39.5-41.7-52.4-52.4-68.7-56.9-146.3-90-233.6-99.6-17.4-1.9-59.8-2.7-76.4-1.4zm78 94.9c77.7 11.8 145.3 46.3 198.2 101.4 51.6 53.6 82.9 119.4 93 195.1 2.4 18.6 2.4 61.8 0 81-5.4 41.6-15.8 75.8-34.2 112.5-29.7 59.3-77.9 110.1-136 143.2-96.4 54.9-215.3 59-315.2 10.8C188.8 693 119.6 603.6 99 498c-3.7-19.2-5.1-32.3-5.7-55.5-.6-25.8.4-42.3 4.2-65.1 16.1-97.1 74.2-183.1 158.8-234.8 45.3-27.8 93.5-43.4 151.2-49 2.2-.2 16.4-.3 31.5-.1 21.7.3 30.4.8 41.5 2.5z"
            />
          </svg>
        </div>
        <input
          class="w-full inline-block py-2 pl-10 pr-4 text-white bg-gray-900 rounded-lg focus:outline-none focus:bg-white focus:text-gray-900"
          placeholder="Search by keywords"
        />
      </div>
      <button
        @click="toggle"
        :class="{ 'bg-gray-600': isOpen, 'bg-gray-700': !isOpen }"
        class="ml-4 pl-3 pr-4 rounded-lg shadow hover:bg-gray-600 focus:outline-none focus:shadow-outline flex items-center"
      >
        <div class="">
          <svg
            class=" w-6 h-6 text-gray-500 fill-current"
            viewBox="-4 0 393 393.99"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M368.313 0H17.05A16.5 16.5 0 002.344 8.96a16.732 16.732 0 001.3 17.415l128.688 181.281c.043.063.09.121.133.184a36.769 36.769 0 017.219 21.816v147.797a16.429 16.429 0 0016.433 16.535c2.227 0 4.426-.445 6.48-1.297l72.313-27.574c6.48-1.976 10.781-8.09 10.781-15.453V229.656a36.774 36.774 0 017.215-21.816c.043-.063.09-.121.133-.184L381.723 26.367a16.717 16.717 0 001.3-17.406A16.502 16.502 0 00368.313 0zM236.78 195.992a56.931 56.931 0 00-11.097 33.664v117.578l-66 25.164V229.656a56.909 56.909 0 00-11.102-33.664L23.648 20h338.07zm0 0"
            />
          </svg>
        </div>
        <span class="ml-1 font-medium text-white">Filters</span>
      </button>
    </div>

    <form
      v-show="isOpen"
      class="xl:h-full xl:flex xl:flex-col xl:justify-between"
    >
      <div class="lg:flex xl:block xl:overflow-y-auto">
        <div
          class="px-4 py-4 border-t border-gray-900 lg:w-1/3 xl:border-t-0  xl:w-full"
        >
          <div class="sm:flex sm:-mx-2">
            <div class="flex flex-wrap -mx-2 sm:w-full sm:mx-0">
              <label class="block w-1/2 px-2 sm:w-1/4 lg:w-1/2" for=""
                ><form-label>Bedrooms</form-label>
                <select class="block w-full mt-1 form-select" name="" id="">
                  <option
                    value="
      "
                    >3</option
                  >
                  <option
                    value="
      "
                    >4</option
                  >
                </select></label
              >

              <label class="block w-1/2 px-2 sm:w-1/4 lg:w-1/2" for="">
                <span class="text-sm font-semibold text-gray-500"
                  >Bathrooms</span
                >
                <select
                  class="block w-full mt-1 text-white shadow form-select"
                  name=""
                  id=""
                >
                  <option value="">4</option>
                </select>
              </label>

              <label
                class="mt-4 block px-2 w-full sm:w-1/2 sm:mt-0 lg:w-full"
                for=""
                ><span class="text-sm font-semibold text-gray-500"
                  >Price Range</span
                >
                <select
                  class="block w-full mt-1 text-white shadow form-select"
                  name=""
                  id=""
                >
                  <option
                    value="
      "
                    >Up to $2,000/wk</option
                  ></select
                ></label
              >
            </div>
          </div>
        </div>
        <div
          class="px-4 py-4 border-t border-gray-900 lg:w-1/3 lg:border-l xl:w-full"
        >
          <span class="block text-sm font-semibold text-gray-500"
            >Property Type</span
          >

          <div class="sm:flex sm:-mx-2 lg:flex lg:flex-col lg:mx-0">
            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-full lg:px-0"
            >
              <input
                class="form-radio"
                type="radio"
                name="propertyType"
                value="house"
              />
              <span class="ml-2 text-white">House</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-full lg:px-0"
            >
              <input
                class="form-radio"
                type="radio"
                name="propertyType"
                value="apartment"
              />
              <span class="ml-2 text-white">Apartment</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-full lg:px-0"
            >
              <input
                class="form-radio"
                type="radio"
                name="propertyType"
                value="loft"
              /><span class="ml-2 text-white">Loft</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-full lg:px-0"
            >
              <input
                class="form-radio"
                type="radio"
                name="propertyType"
                value="townhouse"
              />
              <span class="ml-2 text-white">Townhouse</span>
            </label>
          </div>
        </div>

        <div
          class="px-4 py-4 border-t border-gray-900 lg:w-1/3 lg:border-l  xl:w-full"
        >
          <span class="block font-semibold text-gray-500 text-gray-500 text-sm">
            Amenities</span
          >
          <div class="sm:flex sm:-mx-2 sm:flex-wrap">
            <label class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-1/2">
              <input class="form-checkbox" type="checkbox" name="balcony" />
              <span class="ml-2 text-white"> Balcony</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-1/2 xl:w-full"
            >
              <input
                class="form-checkbox"
                type="checkbox"
                name="airConditioning"
              />
              <span class="ml-2 text-white"> Air conditioning</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-1/2 xl:w-full"
            >
              <input class="form-checkbox" type="checkbox" name="pool" /><span
                class="ml-2 text-white"
                >Pool</span
              >
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-1/2 xl:w-full"
            >
              <input class="form-checkbox" type="checkbox" name="beach" />
              <span class="ml-2 text-white">Beach</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-1/2 xl:w-full"
            >
              <input class="form-checkbox" type="checkbox" name="petFriendly" />
              <span class="ml-2 text-white">Pet friendly</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-1/2 xl:w-full"
            >
              <input class="form-checkbox" type="checkbox" name="kidFriendly" />
              <span class="ml-2 text-white">Kid friendly</span>
            </label>

            <label
              class="flex items-center mt-3 sm:w-1/4 sm:px-2 lg:w-1/2 xl:max-w-full"
            >
              <input class="form-checkbox" type="checkbox" name="parking" />
              <span class="ml-2 text-white">Parking</span>
            </label>
          </div>
        </div>
      </div>

      <div class="px-4 py-4 bg-gray-900 sm:text-right">
        <button
          class="bg-indigo-400 text-white rounded px-2 py-2 font-semibold w-full block sm:inline-block sm:w-auto xl:w-full xl:block"
        >
          Update results
        </button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  props: {},
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
  },

  components: {
    FormLabel: {
      render(h) {
        return h(
          "span",
          {
            class: "text-sm font-semibold text-gray-500",
          },
          this.$slots.default
        );
      },
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
