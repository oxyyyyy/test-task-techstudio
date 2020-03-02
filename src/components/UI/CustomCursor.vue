<template>
  <div class="cursor-field">
    <div class="cursor"></div>
    <div class="cursor-follower"></div>
  </div>
</template>

<script>
import { TweenMax } from "gsap/TweenMax";

let posX = 0,
  posY = 0;

let mouseX = 0,
  mouseY = 0;

window.addEventListener("mousemove", function() {
  mouseX = event.pageX - window.scrollX;
  mouseY = event.pageY - window.scrollY;
});

export default {
  name: "CustomCursor",
  mounted: function() {
    TweenMax.to({}, 0.016, {
      repeat: -1,
      onRepeat: function() {
        posX += (mouseX - posX) / 9;
        posY += (mouseY - posY) / 9;

        TweenMax.set(".cursor-follower", {
          css: {
            left: posX - 12,
            top: posY - 12
          }
        });
        TweenMax.set(".cursor", {
          css: {
            left: mouseX,
            top: mouseY
          }
        });
      }
    });

    document.querySelectorAll("a, button").forEach(item => {
      item.addEventListener("mouseenter", function() {
        document.querySelectorAll(".cursor")[0].classList.add("active");
        document
          .querySelectorAll(".cursor-follower")[0]
          .classList.add("active");
      });
      item.addEventListener("mouseout", function() {
        document.querySelectorAll(".cursor")[0].classList.remove("active");
        document
          .querySelectorAll(".cursor-follower")[0]
          .classList.remove("active");
      });
    });
  }
};
</script>

<style lang="scss">
body {
  cursor: none;
}

.cursor-field {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 999;
  pointer-events: none;
  mix-blend-mode: difference;
}

.cursor {
  position: absolute;
  background: #fff;
  width: 6px;
  height: 6px;
  border-radius: 100%;
  z-index: 10000;
  transform: scale(1);
  user-select: none;
  pointer-events: none;
  transition: 0.3s ease-in-out transform, 0.2s ease-in-out opacity;

  &.active {
    opacity: 0.5;
    transform: scale(0);
  }

  &.hovered {
    opacity: 0.08;
  }
}

.cursor-follower {
  position: absolute;
  background-color: rgba(255, 255, 255, 0.3);
  width: 20px;
  height: 20px;
  border-radius: 100%;
  z-index: 10000;
  transform: translatex(5px, 5px);
  user-select: none;
  pointer-events: none;
  transition: 0.6s ease-in-out transform, 0.2s ease-in-out opacity;

  &.active {
    opacity: 0.7;
    transform: scale(3);
  }
  &.hovered {
    opacity: 0.08;
  }
}

a,
button {
  cursor: none;
}
</style>
