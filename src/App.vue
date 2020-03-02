<template>
  <div id="app">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import "normalize.css";

import Navbar from "@/components/Navbar";

export default {
  components: {
    Navbar
  }
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}

#app {
  font-family: "Gilroy", sans-serif;
  font-weight: normal;
  font-style: normal;
  font-size: 18px;
  color: $font-color;
  padding-top: 96px;
}

a {
  text-decoration: none;
  color: $font-color;
  transition: color 0.12s;

  &:hover {
    color: $font-accent-color;
  }
}

ul,
ol {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 1310px;
  padding: 0 15px;
  margin: 0 auto;
}
</style>
