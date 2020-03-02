<template>
  <div class="home">
    <Services />
  </div>
</template>

<script>
import Services from "@/components/sections/Services.vue";

export default {
  name: "Home",
  components: {
    Services
  }
};
</script>

<style lang="scss" scoped>
.home {
  background-color: #fff;
}
</style>
