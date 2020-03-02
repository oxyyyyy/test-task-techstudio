<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__top">
        <h3 class="footer__title">Связаться с нами</h3>
        <p class="footer__text">
          У нас работают очень милые консультанты, готовые ответить на ваши
          вопросы, помочь с подбором материала и типа печати и просчитать
          стоимость заказа
        </p>
        <CtaButton title="задать вопрос онлайн" link="/contact-form" />
      </div>
      <div class="footer__bottom">
        <div class="footer__links-container">
          <h6 class="footer__links-title">Написать</h6>
          <a href="#" class="footer__link-item">facebook</a>
          <a href="#" class="footer__link-item">telegram</a>
          <a href="#" class="footer__link-item">viber</a>
        </div>
        <div class="footer__links-container">
          <h6 class="footer__links-title">Позвонить</h6>
          <a href="tel:+380990001345" class="footer__link-item"
            >099 000 1 345</a
          >
          <a href="tel:+380990001345" class="footer__link-item"
            >099 000 1 345</a
          >
          <a href="tel:+380990001345" class="footer__link-item"
            >099 000 1 345</a
          >
        </div>
        <address class="footer__links-container">
          <h6 class="footer__links-title">Прийти</h6>
          <p class="footer__link-item">Киев, Украина</p>
          <a
            href="https://goo.gl/maps/2QU1D3iqQwCgYpKm9"
            class="footer__link-item"
            target="_blank"
            >Саксаганского, 6а</a
          >
          <p class="footer__link-item">10:00 — 22:00, каждый день</p>
        </address>
      </div>
    </div>
  </footer>
</template>

<script>
import CtaButton from "@/components/UI/CtaButton";

export default {
  name: "Footer",
  components: {
    CtaButton
  }
};
</script>

<style lang="scss" scoped>
.footer {
  color: #fbfbfb;
  background: #191919;
  padding-top: 150px;
  padding-bottom: 60px;

  @media screen and (max-width: $breakpoint-mobile) {
    padding-top: 75px;
    padding-bottom: 30px;
  }
}

.footer__top {
  max-width: 510px;
  margin-bottom: 130px;

  @media screen and (max-width: $breakpoint-mobile) {
    margin-bottom: 50px;
  }
}

.footer__title {
  font-weight: 600;
  font-size: 56px;
  line-height: 170%;
  margin: 0;
  margin-bottom: 12px;

  @media screen and (max-width: $breakpoint-mobile) {
    font-size: 28px;
  }
}

.footer__text {
  line-height: 170%;
  margin: 0;
  margin-bottom: 32px;
}

.footer__links-title {
  font-weight: bold;
  font-size: 20px;
  line-height: (24/20);
  color: #f3f3f3;
  margin: 0;
  margin-bottom: 18px;
}

.footer__link-item {
  display: block;
  line-height: (21/18);
  color: #f3f3f3;
  margin: 0;
  transition: all 0.2s ease;

  &:not(:last-child) {
    margin-bottom: 16px;
  }
}

a.footer__link-item {
  &:hover {
    color: #8e8e8e;
  }
}

.footer__bottom {
  display: flex;
  justify-content: flex-end;
  align-items: flex-start;

  @media screen and (max-width: $breakpoint-mobile) {
    flex-direction: column;
  }
}

.footer__links-container {
  &:not(:first-child) {
    margin-left: 160px;

    @media screen and (max-width: $breakpoint-tablet) {
      margin-left: 75px;
    }

    @media screen and (max-width: $breakpoint-mobile) {
      margin-left: 0;
      margin-top: 30px;
    }
  }
}
</style>
