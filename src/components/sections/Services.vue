<template>
  <section class="services">
    <div class="container">
      <header class="services__header">
        <h1 class="services__title">Что мы делаем</h1>
        <p class="services__text">
          Urbanprint работает на рынке широкоформатной печати уже 8 лет. За эти
          годы мы создали тонны рекламной продукции и не собираемся
          останавливаться на этих цифрах.<br />С нашей помощью вы сможете
          оформить свой бизнес от визиток и листовок до витрин и билбордов.<br />Давайте
          посмотрим, что мы можем для вас сделать.
        </p>
      </header>
      <main class="services__body">
        <div class="services__cards-list">
          <ServicesCard :card="card" v-for="card in cards" :key="card.id" />
        </div>
      </main>
    </div>
  </section>
</template>

<script>
import ServicesCard from "@/components/ServicesCard.vue";

export default {
  name: "Services",
  components: {
    ServicesCard
  },
  data() {
    return {
      cards: [
        {
          id: "card-0",
          title: "Широкоформатная печать",
          innerLinks: [
            {
              id: 0,
              title: "Лайтбоксы",
              link: "/some-route"
            },
            {
              id: 1,
              title: "Объёмные буквы",
              link: "/some-route"
            },
            {
              id: 2,
              title: "Вывески",
              link: "/some-route"
            },
            {
              id: 3,
              title: "Штендеры",
              link: "/some-route"
            },
            {
              id: 4,
              title: "Каркасы",
              link: "/some-route"
            },
            {
              id: 5,
              title: "Монтаж",
              link: "/some-route"
            },
            {
              id: 6,
              title: "Фрезерная порезка",
              link: "/some-route"
            },
            {
              id: 7,
              title: "Лазерная порезка",
              link: "/some-route"
            }
          ]
        },
        {
          id: "card-1",
          title: "Ультрафиолетовая печать",
          innerLinks: [
            {
              id: 0,
              title: "Лайтбоксы",
              link: "/some-route"
            },
            {
              id: 1,
              title: "Объёмные буквы",
              link: "/some-route"
            },
            {
              id: 2,
              title: "Вывески",
              link: "/some-route"
            },
            {
              id: 3,
              title: "Штендеры",
              link: "/some-route"
            },
            {
              id: 4,
              title: "Каркасы",
              link: "/some-route"
            },
            {
              id: 5,
              title: "Монтаж",
              link: "/some-route"
            },
            {
              id: 6,
              title: "Фрезерная порезка",
              link: "/some-route"
            },
            {
              id: 7,
              title: "Лазерная порезка",
              link: "/some-route"
            }
          ]
        },
        {
          id: "card-2",
          title: "Наружная реклама",
          innerLinks: [
            {
              id: 0,
              title: "Лайтбоксы",
              link: "/some-route"
            },
            {
              id: 1,
              title: "Объёмные буквы",
              link: "/some-route"
            },
            {
              id: 2,
              title: "Вывески",
              link: "/some-route"
            },
            {
              id: 3,
              title: "Штендеры",
              link: "/some-route"
            },
            {
              id: 4,
              title: "Каркасы",
              link: "/some-route"
            },
            {
              id: 5,
              title: "Монтаж",
              link: "/some-route"
            },
            {
              id: 6,
              title: "Фрезерная порезка",
              link: "/some-route"
            },
            {
              id: 7,
              title: "Лазерная порезка",
              link: "/some-route"
            }
          ]
        },
        {
          id: "card-3",
          title: "Конструкции",
          innerLinks: [
            {
              id: 0,
              title: "Лайтбоксы",
              link: "/some-route"
            },
            {
              id: 1,
              title: "Объёмные буквы",
              link: "/some-route"
            },
            {
              id: 2,
              title: "Вывески",
              link: "/some-route"
            },
            {
              id: 3,
              title: "Штендеры",
              link: "/some-route"
            },
            {
              id: 4,
              title: "Каркасы",
              link: "/some-route"
            },
            {
              id: 5,
              title: "Монтаж",
              link: "/some-route"
            },
            {
              id: 6,
              title: "Фрезерная порезка",
              link: "/some-route"
            },
            {
              id: 7,
              title: "Лазерная порезка",
              link: "/some-route"
            }
          ]
        },
        {
          id: "card-4",
          title: "Полиграфия",
          innerLinks: [
            {
              id: 0,
              title: "Лайтбоксы",
              link: "/some-route"
            },
            {
              id: 1,
              title: "Объёмные буквы",
              link: "/some-route"
            },
            {
              id: 2,
              title: "Вывески",
              link: "/some-route"
            },
            {
              id: 3,
              title: "Штендеры",
              link: "/some-route"
            },
            {
              id: 4,
              title: "Каркасы",
              link: "/some-route"
            },
            {
              id: 5,
              title: "Монтаж",
              link: "/some-route"
            },
            {
              id: 6,
              title: "Фрезерная порезка",
              link: "/some-route"
            },
            {
              id: 7,
              title: "Лазерная порезка",
              link: "/some-route"
            }
          ]
        },
        {
          id: "card-5",
          title: "Дизайн",
          innerLinks: [
            {
              id: 0,
              title: "Лайтбоксы",
              link: "/some-route"
            },
            {
              id: 1,
              title: "Объёмные буквы",
              link: "/some-route"
            },
            {
              id: 2,
              title: "Вывески",
              link: "/some-route"
            },
            {
              id: 3,
              title: "Штендеры",
              link: "/some-route"
            },
            {
              id: 4,
              title: "Каркасы",
              link: "/some-route"
            },
            {
              id: 5,
              title: "Монтаж",
              link: "/some-route"
            },
            {
              id: 6,
              title: "Фрезерная порезка",
              link: "/some-route"
            },
            {
              id: 7,
              title: "Лазерная порезка",
              link: "/some-route"
            }
          ]
        }
      ],
      cardIsActive: ""
    };
  }
};
</script>

<style lang="scss" scoped>
.services {
  padding-top: 100px;
  padding-bottom: 285px;
  position: relative;
  overflow: hidden;

  &::before {
    content: "";
    width: 580px;
    height: 580px;
    background: #eff7fd;
    border-radius: 999px;
    position: absolute;
    bottom: 120px;
    right: 435px;
    animation: bubbleFloat 10s ease-in-out 0s infinite both;

    @media screen and (max-width: $breakpoint-tablet) {
      right: 50%;
      transform: translateX(50%);
      animation: none;
    }
  }

  @media screen and (max-width: $breakpoint-tablet) {
    padding-top: 50px;
    padding-bottom: 100px;
  }

  @media screen and (max-width: $breakpoint-tablet) {
    padding-bottom: 50px;
  }
}

.services__header {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 105px;
  align-items: center;
  padding-bottom: 90px;

  @media screen and (max-width: $breakpoint-tablet) {
    grid-template-columns: auto;
    grid-gap: 30px;
    padding-bottom: 50px;
  }
}

.services__title {
  font-weight: 600;
  font-size: 56px;
  margin: 0;
}

.services__text {
  line-height: 170%;
  margin: 0;
}

.services__cards-list {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 40px;

  @media screen and (max-width: $breakpoint-tablet) {
    grid-template-columns: repeat(2, 1fr);
  }

  @media screen and (max-width: $breakpoint-mobile) {
    grid-template-columns: auto;
  }
}

@keyframes bubbleFloat {
  from {
    transform: translateY(0) scale(1);
  }

  50% {
    transform: translateY(-6%) scale(1.06);
  }

  to {
    transform: translateY(0) scale(1);
  }
}
</style>
