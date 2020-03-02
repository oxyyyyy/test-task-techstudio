<template>
  <button
    :to="link"
    class="cta-btn"
    ref="ctaBtn"
    @mouseenter="onMouseEnter"
    @mouseout="onMouseOut"
  >
    <p>{{ title }}</p>
    <span :style="{ top: top + 'px', left: left + 'px' }"></span>
  </button>
</template>

<script>
export default {
  name: "CtaButton",
  data() {
    return {
      top: null,
      left: null
    };
  },
  props: {
    link: String,
    title: String
  },
  methods: {
    onMouseEnter(event) {
      const element = this.$el;
      const x = event.pageX - element.offsetLeft;
      const y = event.pageY - element.offsetTop;
      this.top = y;
      this.left = x;
    },
    onMouseOut(event) {
      const element = this.$el;
      const x = event.pageX - element.offsetLeft;
      const y = event.pageY - element.offsetTop;
      this.top = y;
      this.left = x;
    }
  }
};
</script>

<style lang="scss" scoped>
.cta-btn {
  font-weight: 500;
  line-height: 100%;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  color: #fbfbfb;
  padding: 16px 40px;
  border: 1px solid #fbfbfb;
  position: relative;
  overflow: hidden;
  transition: all 0.4s ease-in-out;
  z-index: 5;

  p {
    position: relative;
    z-index: 10;
    margin: 0;
  }

  span {
    position: absolute;
    display: block;
    width: 0;
    height: 0;
    border-radius: 50%;
    background-color: #fbfbfb;
    transition: height 0.4s ease-in-out, width 0.4s ease-in-out;
    transform: translate(-50%, -50%);
    z-index: 3;
  }

  &:hover {
    color: #191919;

    span {
      width: 600px;
      height: 600px;
    }
  }

  &:active {
    background-color: #fbfbfb;
  }
}
</style>
