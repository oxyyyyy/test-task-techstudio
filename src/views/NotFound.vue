<template>
  <div class="notFound">
    <h1 class="notFound__title">404</h1>
  </div>
</template>

<script>
export default {
  name: "NotFound"
};
</script>

<style lang="scss" scoped>
.notFound {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 10vh;
  background-color: #fff;
}

.notFound__title {
  font-size: 10rem;
}
</style>
