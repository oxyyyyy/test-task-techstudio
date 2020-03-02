<template>
  <div id="app">
    <Navbar />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import "normalize.css";

import Navbar from "@/components/Navbar";
import Footer from "@/components/sections/Footer";

export default {
  components: {
    Navbar,
    Footer
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

address {
  font-style: normal;
}

button {
  background-color: initial;
  border: initial;
  cursor: pointer;
}

.container {
  max-width: 1310px;
  padding: 0 15px;
  margin: 0 auto;
}
</style>
