<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__inner">
        <div class="footer__top">
          <div class="footer__left-column">
            <div class="footer__logo">
              <a href="#"><img src="../public/img/icons/logo.png" alt="Logo" /></a>
            </div>
            <p class="footer__text">
              SMMSMM - сервис, где вы сможете приобрести качественное
              продвижение в социальных сетях по выгодным ценам.
            </p>
            <nav class="footer__list-wrapper">
              <ul class="footer__list">
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#">Услуги</a>
                </li>
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#">Отзывы</a>
                </li>
              </ul>
              <ul class="footer__list">
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#"
                    >Как это работает</a
                  >
                </li>
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#">Преимущества</a>
                </li>
              </ul>
              <ul class="footer__list">
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#"
                    >SMMFlow vs Другие сайты</a
                  >
                </li>
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#">Частые вопросы</a>
                </li>
              </ul>
              <ul class="footer__list">
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#">Правила сервиса</a>
                </li>
                <li class="footer__list-item">
                  <a class="footer__list-item-link" href="#">Контакты</a>
                </li>
              </ul>
            </nav>
          </div>
          <div class="footer__right-column">
            <div class="footer__form-inner">
              <h5 class="footer__form-title">Нужна помощь?</h5>
              <div
                class="footer__form-input-wrapper footer__form-input-wrapper-chat"
              >
                <input
                  class="footer__form-input"
                  type="text"
                  placeholder="Чат с поддержкой"
                />
              </div>
              <div
                class="footer__form-input-wrapper footer__form-input-wrapper-email"
              >
                <input
                  class="footer__form-input"
                  type="email"
                  placeholder="support@smmsmm.net"
                />
              </div>
            </div>
          </div>
        </div>
        <div class="footer__bottom">
          <div class="footer__bottom-left">
            <ul class="footer__bottom-list">
              <li class="footer__bottom-list-item">
                <a class="footer__bottom-list-item-link" href="#"
                  >Политика конфиденциальности</a
                >
              </li>
              <li class="footer__bottom-list-item">
                <a class="footer__bottom-list-item-link" href="#"
                  >Публичная оферта</a
                >
              </li>
              <li class="footer__bottom-list-item">
                <a class="footer__bottom-list-item-link" href="#"
                  >Пользовательское соглашение</a
                >
              </li>
            </ul>
          </div>
          <div class="footer__bottom-right">
            <IconMIR />
            <IconVISA />
            <IconMasterCard />
            <IconQIWI />
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import IconMIR from "./icons/IconMIR.vue";
import IconVISA from "./icons/IconVISA.vue";
import IconMasterCard from "./icons/IconMasterCard.vue";
import IconQIWI from "./icons/IconQIWI.vue";

export default {
  name: 'TheFooter',
  components: {
    IconMIR,
    IconVISA,
    IconMasterCard,
    IconQIWI,
  },
};
</script>


<style scoped lang="scss">
.footer {
  background: #f9f9f9;
  &__inner {
    padding-top: 3.2rem;
    padding-bottom: 2.4rem;
  }

  &__top {
    display: flex;
    justify-content: space-between;
  }

  &__left-column {
  }

  &__logo {
    margin-bottom: 2.4rem;
  }

  &__text {
    font-family: "Nunito Sans";
    font-style: normal;
    font-weight: 400;
    font-size: 1.8rem;
    line-height: 160%;
    color: #676767;
    max-width: 54rem;
    margin-bottom: 4.8rem;
  }

  &__list-wrapper {
    display: flex;
    margin-bottom: 4.8rem;
  }

  &__list {
    &:not(:last-child) {
      margin-right: 5.6rem;
    }
  }

  &__list-item {
    &:not(:last-child) {
      margin-bottom: 1.2rem;
    }
  }

  &__list-item-link {
    font-family: "Nunito Sans";
    font-style: normal;
    font-weight: 400;
    font-size: 1.6rem;
    line-height: 160%;
    color: #676767;
  }

  &__right-column {
  }

  &__form-inner {
    background: #ffffff;
    border-radius: 24px;
    padding: 2.4rem;
    display: flex;
    flex-direction: column;
    // max-width: 31.8rem;
    // width: 100%;
  }

  &__form-title {
    font-family: "Nunito Sans";
    font-style: normal;
    font-weight: 600;
    font-size: 1.8rem;
    line-height: 133%;
    color: #676767;
    margin-bottom: 1.6rem;
  }

  &__form-input-wrapper {
    position: relative;

    &:not(:last-child) {
      margin-bottom: 1.2rem;
    }

    &::before {
      position: absolute;
      content: "";
      top: 50%;
      left: 20px;
      transform: translate(0, -50%);
      z-index: 5;
    }
  }

  &__form-input-wrapper-chat {
    &::before {
      content: url(img/icons/Chat.svg);
    }
  }

  &__form-input-wrapper-email {
    &::before {
      content: url(img/icons/E-mail.svg);
    }
  }

  &__form-input {
    font-family: "Nunito Sans";
    font-style: normal;
    font-weight: 400;
    font-size: 1.8rem;
    line-height: 160%;
    color: #676767;
    border: 1px solid #e0e0e0;
    border-radius: 16px;
    padding: 1.15rem 2rem 1.15rem 6rem;
  }

  &__bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__bottom-left {
  }

  &__bottom-list {
    display: flex;
    align-items: center;
    gap: 5.6rem;
  }

  &__bottom-list-item {
  }

  &__bottom-list-item-link {
    font-family: "Nunito Sans";
    font-style: normal;
    font-weight: 400;
    font-size: 1.6rem;
    line-height: 160%;
    color: #b0b0b0;
  }

  &__bottom-right {
    display: flex;
    align-items: center;
    gap: 1.2rem;
  }
}
</style>