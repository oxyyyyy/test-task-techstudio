<template>
  <div>
    <div class="nav" :class="{ active: menuIsActive }">
      <div class="nav__container nav__phone-container">
        <a href="tel:+380990002111">+38 099 000 2 111</a>
      </div>
      <router-link to="/" class="nav__container nav__logo-container">
        <img src="@/assets/img/logo.svg" alt="" />
      </router-link>
      <div class="nav__container">
        <div
          class="menu-toggle"
          :class="{ active: menuIsActive }"
          @click="toggleMenu"
        >
          <div class="menu-toggle__one"></div>
          <div class="menu-toggle__two"></div>
          <div class="menu-toggle__three"></div>
        </div>
      </div>
    </div>
    <div class="fs-menu" :class="{ active: menuIsActive }">
      <div class="fs-menu__body">
        <ul class="fs-menu__main-links-list">
          <li v-for="item in menuLinks" :key="item.id">
            <router-link
              :to="item.link"
              class="fs-menu__body-item fs-menu__body-item--big"
            >
              {{ item.title }}
            </router-link>
          </li>
        </ul>
        <ul class="fs-menu__sub-links-list">
          <li v-for="item in subMenuLinks" :key="item.id">
            <router-link :to="item.link" class="fs-menu__body-item">
              {{ item.title }}
            </router-link>
          </li>
        </ul>
      </div>
      <div class="fs-menu__footer">
        <address class="fs-menu__container">
          <p class="fs-menu__footer-item">Киев, Украина</p>
          <a
            href="https://goo.gl/maps/2QU1D3iqQwCgYpKm9"
            class="fs-menu__footer-item"
            target="_blank"
            >Саксаганского, 6а</a
          >
          <p class="fs-menu__footer-item">10:00 — 22:00, каждый день</p>
        </address>
        <div class="fs-menu__container">
          <a href="#" class="fs-menu__footer-item">facebook</a>
          <a href="#" class="fs-menu__footer-item">telegram</a>
          <a href="#" class="fs-menu__footer-item">viber</a>
        </div>
        <div class="fs-menu__container">
          <a href="tel:+380990001345" class="fs-menu__footer-item"
            >099 000 1 345</a
          >
          <a href="tel:+380990001345" class="fs-menu__footer-item"
            >099 000 1 345</a
          >
          <a href="tel:+380990001345" class="fs-menu__footer-item"
            >099 000 1 345</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      menuIsActive: false,
      menuLinks: [
        {
          id: 0,
          title: "Широкоформатная печать",
          link: "/some-route-1"
        },
        {
          id: 1,
          title: "Ультрафиолетовая печать",
          link: "/some-route-2"
        },
        {
          id: 2,
          title: "Наружная реклама",
          link: "/some-route-3"
        },
        {
          id: 3,
          title: "Конструкции",
          link: "/some-route-4"
        },
        {
          id: 4,
          title: "Полиграфия",
          link: "/some-route-5"
        },
        {
          id: 5,
          title: "Дизайн",
          link: "/some-route-6"
        },
        {
          id: 6,
          title: "Контакты",
          link: "/some-route-7"
        }
      ],
      subMenuLinks: [
        {
          id: 7,
          title: "Лайтбоксы",
          link: "/some-route-8"
        },
        {
          id: 8,
          title: "Объёмные буквы",
          link: "/some-route-9"
        },
        {
          id: 9,
          title: "Вывески",
          link: "/some-route-10"
        },
        {
          id: 10,
          title: "Штендеры",
          link: "/some-route-11"
        },
        {
          id: 11,
          title: "Каркасы",
          link: "/some-route-12"
        },
        {
          id: 12,
          title: "Монтаж",
          link: "/some-route-13"
        },
        {
          id: 13,
          title: "Фрезерная порезка",
          link: "/some-route-14"
        },
        {
          id: 14,
          title: "Лазерная порезка",
          link: "/some-route-7"
        }
      ]
    };
  },
  methods: {
    toggleMenu() {
      this.menuIsActive = !this.menuIsActive;
    }
  }
};
</script>

<style lang="scss" scopped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px 40px;
  background: #ffffff;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 600;
  transition: all $trans-prop;

  a {
    transition: opacity $trans-prop;
  }

  img {
    transition: opacity $trans-prop;
  }

  &.active {
    background-color: transparent;
    transition: none;

    a {
      opacity: 0;
    }

    img {
      opacity: 0;
    }
  }
}

.menu-toggle {
  width: 40px;
  height: 30px;
  cursor: pointer;
  position: relative;
  z-index: 800;

  &.active {
    .menu-toggle__one {
      transform: rotate(45deg) translate(7px, 7px);
      background: $fs-menu-font-color;
    }

    .menu-toggle__two {
      opacity: 0;
      background: $fs-menu-font-color;
    }

    .menu-toggle__three {
      transform: rotate(-45deg) translate(8px, -10px);
      background: $fs-menu-font-color;
    }
  }
}

.menu-toggle__one,
.menu-toggle__two,
.menu-toggle__three {
  width: 100%;
  height: 5px;
  background: $font-color;
  margin: 6px auto;
  backface-visibility: hidden;
  transition-duration: 0.3s;
}

.fs-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: $fs-menu-bg;
  z-index: 500;
  opacity: 0;
  visibility: hidden;
  transition: all $trans-prop;
  color: $fs-menu-font-color;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  overflow-x: hidden;
  overflow-y: auto;

  &.active {
    opacity: 1;
    visibility: visible;
  }

  a {
    color: $fs-menu-font-color;
    display: block;
  }
}

.fs-menu__body {
  display: flex;
  align-items: flex-start;
  padding: 23.4vh 2.9% 30px 7.3%;

  @media screen and (max-width: $breakpoint-mobile) {
    flex-direction: column;
  }
}

.fs-menu__body-item {
  font-size: 18px;
  transition: all $trans-prop;
}

.fs-menu__body-item--big {
  font-size: 24px;
  position: relative;

  &::before {
    content: "";
    position: absolute;
    top: 50%;
    left: -40px;
    transform: translateY(-50%) scale(0.8);
    opacity: 0;
    border: 1px solid #f3f3f3;
    width: 60px;
    height: 60px;
    border-radius: 999px;
    transition: all $trans-prop;
  }
}

.fs-menu__main-links-list {
  margin-right: 25.8%;

  @media screen and (max-width: $breakpoint-mobile) {
    margin-right: 0;
    margin-bottom: 60px;
  }

  li:not(:last-child) {
    margin-bottom: 30px;
  }

  .fs-menu__body-item {
    &:hover,
    &.router-link-active {
      transform: translateX(0.8rem);
      color: $font-accent-color;

      &::before {
        opacity: 0.3;
        transform: translateY(-50%) scale(1);
      }
    }
  }
}

.fs-menu__sub-links-list {
  position: relative;

  li:not(:last-child) {
    margin-bottom: 24px;
  }

  .fs-menu__body-item {
    &:hover,
    &.router-link-active {
      color: $font-accent-color;
    }
  }

  &::before {
    content: "";
    width: 500px;
    height: 500px;
    background: #fbfbfb;
    opacity: 0.03;
    border: 1px solid #f3f3f3;
    border-radius: 9999px;
    position: absolute;
    top: 50%;
    left: 70%;
    transform: translate(-50%, -50%);
    pointer-events: none;
  }
}

.fs-menu__footer {
  display: flex;
  justify-content: space-between;
  padding: 30px 2.9% 30px 7.3%;

  @media screen and (max-width: $breakpoint-mobile) {
    flex-direction: column;
  }

  .fs-menu__container {
    @media screen and (max-width: $breakpoint-mobile) {
      margin-bottom: 30px;
    }
  }
}

.fs-menu__footer-item {
  margin: 0;

  &:not(:last-child) {
    margin-bottom: 14px;
  }
}

.nav__phone-container {
  @media screen and (max-width: $breakpoint-mobile) {
    display: none;
  }
}

.nav__logo-container {
  position: absolute;
  top: 53.5%;
  left: 50%;
  transform: translate(-50%, -50%);
  @media screen and (max-width: $breakpoint-mobile) {
    position: relative;
    left: initial;
    top: 5px;
    transform: none;
  }
}
</style>
