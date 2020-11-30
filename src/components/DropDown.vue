<template>
  <div class="relative">
    <button @click="toggle" type="button" class="block focus:outline-none" @focus="buttonHasFocus=true" @blur="buttonHasFocus=false">
        <slot name="trigger" :hasFocus="buttonHasFocus" :isOpen="isOpen"></slot>
    </button>

    <div :class="[isOpen ? 'block' : 'hidden']">
      <button
        @click="isOpen = false"
        type="button"
        class="block  fixed opacity-0 inset-0 cursor-default w-full h-full z-30 "
      ></button>

<div class="absolute z-40 right-0">
      <slot name="dropdown"></slot>

</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {},
  data() {
    return {
      // isOpen: true,
      isOpen: false,
      buttonHasFocus: false
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
  },
  mounted() {
    const onEscape = (e) => {
      if (!this.isOpen || e.key !== "Escape") {
        return;
      }
      this.isOpen = false;
    };
    document.addEventListener("keydown", onEscape);
    this.$on("hook:destroyed", () => {
      document.removeEventListener("keydown", onEscape);
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
