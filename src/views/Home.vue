<template>
  <div class="home" :class="{ mounted: homeIsMounted }">
    <Services />
  </div>
</template>

<script>
import Services from "@/components/sections/Services.vue";

export default {
  name: "Home",
  data() {
    return {
      homeIsMounted: false
    };
  },
  components: {
    Services
  },
  mounted() {
    setTimeout(() => {
      this.homeIsMounted = true;
    }, 200);
  }
};
</script>

<style lang="scss" scoped>
.home {
  background-color: #fff;
  opacity: 0;
  transition: all 0.4s ease-in-out;

  &.mounted {
    opacity: 1;
  }
}
</style>
