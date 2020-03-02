<template>
  <div id="app">
    <Navbar />
    <router-view />
    <Footer />
    <CustomCursor />
  </div>
</template>

<script>
import "normalize.css";

import CustomCursor from "@/components/UI/CustomCursor";
import Navbar from "@/components/Navbar";
import Footer from "@/components/sections/Footer";

export default {
  components: {
    Navbar,
    Footer,
    CustomCursor
  }
};
</script>

<style lang="scss">
@font-face {
  font-family: "Gilroy";
  font-weight: normal;
  font-style: normal;
  src: url("/fonts/Gilroy/Gilroy-Regular.eot");
  src: url("/fonts/Gilroy/Gilroy-Regular?#iefix") format("embedded-opentype"),
    url("/fonts/Gilroy/Gilroy-Regular.woff2") format("woff2"),
    url("/fonts/Gilroy/Gilroy-Regular.woff") format("woff"),
    url("/fonts/Gilroy/Gilroy-Regular.ttf") format("truetype");
}

@font-face {
  font-family: "Gilroy";
  font-weight: 500;
  font-style: normal;
  src: url("/fonts/Gilroy/Gilroy-Medium.eot");
  src: url("/fonts/Gilroy/Gilroy-Medium?#iefix") format("embedded-opentype"),
    url("/fonts/Gilroy/Gilroy-Medium.woff2") format("woff2"),
    url("/fonts/Gilroy/Gilroy-Medium.woff") format("woff"),
    url("/fonts/Gilroy/Gilroy-Medium.ttf") format("truetype");
}

@font-face {
  font-family: "Gilroy";
  font-weight: 600;
  font-style: normal;
  src: url("/fonts/Gilroy/Gilroy-Semibold.eot");
  src: url("/fonts/Gilroy/Gilroy-Semibold?#iefix") format("embedded-opentype"),
    url("/fonts/Gilroy/Gilroy-Semibold.woff2") format("woff2"),
    url("/fonts/Gilroy/Gilroy-Semibold.woff") format("woff"),
    url("/fonts/Gilroy/Gilroy-Semibold.ttf") format("truetype");
}

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
  cursor: none;
  padding: 0;
  outline: none;
}

.container {
  max-width: 1310px;
  padding: 0 15px;
  margin: 0 auto;
}
</style>
