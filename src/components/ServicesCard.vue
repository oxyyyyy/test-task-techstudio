<template>
  <div class="services__card-item-deck">
    <div class="services__card-item">
      <div class="services__card-face services__card-face--front">
        <h6 class="services__card-title">{{ card.title }}</h6>
      </div>
      <div class="services__card-face services__card-face--back">
        <router-link
          :to="cardInnerLink.link"
          v-for="cardInnerLink in card.innerLinks"
          :key="cardInnerLink.id"
          class="services__card-inner-links"
        >
          {{ cardInnerLink.title }}
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServicesCard",
  props: {
    card: {
      type: Object,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
.services__card-item {
  background: #ffffff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.15);
  border-radius: 4px;
  min-height: 260px;
  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  transition: all 0.35s linear;
}

.services__card-title {
  font-weight: 500;
  font-size: 24px;
  line-height: 167%;
  letter-spacing: 0.045em;
  margin: 0;
}

.services__card-item-deck {
  position: relative;
  perspective: 1000px;
}

.services__card-face {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 10px;
  padding: 40px 50px 40px 40px;
}

.services__card-face--back {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(6, 1fr);
  grid-auto-flow: column;
  grid-row-gap: 16px;
  align-items: center;
  overflow: hidden;
  z-index: -1;
  transform: rotateY(180deg);
  padding: 40px;

  &:before {
    content: "";
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: -1;
    background-size: 100% 100%;
    transform: rotateY(180deg);
  }
}

.services__card-inner-links {
  margin: 0;
  font-size: 14px;
  line-height: (16/14);
}

.services__card-face--front {
  z-index: 1;
  display: flex;
  align-items: center;
}

.services__card-face--front,
.services__card-face--back {
  transition: all 0.35s linear;
}

.services__card-item-deck:hover .services__card-item {
  transform: rotateY(180deg);
}
</style>
