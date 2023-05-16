<script setup>
useSeoMeta({
  title: 'My Amazing Site',
  ogTitle: 'My Amazing Site',
  description: 'This is my amazing site, let me tell you all about it.',
  ogDescription: 'This is my amazing site, let me tell you all about it.',
  ogImage: 'https://example.com/image.png',
  twitterCard: 'summary_large_image',
})
</script>


<template>
  <section class="hero">
    <div class="container">
      <div class="hero__inner">
        <div class="hero__content">
          <h1 class="hero__title">
            Продвижение во всех соцсетях за пару кликов
          </h1>
          <h2 class="hero__subtitle">
            Получайте подписчиков, лайки, репосты, просмотры, прослушивания и
            любую другую активность на свои профили в социальных сетях по самым
            низким ценам на рынке и в самые быстрые сроки!
          </h2>
          <div class="hero__buttons">
            <v-btn
              class="hero__button"
              title="Начать продвижение"
              @click="clickBtn"
              :disabled="false"
              :success="true"
              :orange="true"
            >
            </v-btn>
          </div>
          <div class="hero__ratings">
            <div class="hero__ratings-stars-numbers">
              <div class="hero__ratings-stars">
                <IconStar />
                <IconStar />
                <IconStar />
                <IconStar />
                <IconStar />
              </div>
              <div class="hero__ratings-numbers">4.4 / 5</div>
            </div>
            <div class="hero__ratings-descr">По данным 693 отзывов</div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <div class="quick-order">
    <div class="container">
      <div class="quick-order__inner">
        <h2 class="quick-order__title">Быстрый заказ</h2>
        <div class="quick-order__list-wrapper">
          <div class="quick-order__list-inner">
            <div class="quick-order__list-title">
              Сначала выберите социальную сеть
            </div>
            <div class="quick-order__list">
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-instagram"
                title="Instagram"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-twitter"
                title="Twitter"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-vk"
                title="VK"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-youtube"
                title="YouTube"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-telegram"
                title="Telegram"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-facebook"
                title="Facebook"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-tiktok"
                title="TikTok"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-social quick-order__button-twitch"
                title="Twitch"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
            </div>
            <v-btn
              class="quick-order__button quick-order__button-social quick-order__button-rutube"
              title="RuTube"
              @click="clickBtn"
              :grey="true"
            >
            </v-btn>
          </div>
          <div class="quick-order__list-inner">
            <div class="quick-order__list-title">Затем выберите услугу</div>
            <div class="quick-order__list">
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-subscribers"
                title="Подписчики"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-spectator"
                title="Зрители"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-likes"
                title="Лайки"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-statistics"
                title="Статистика"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-views"
                title="Просмотры"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-IGTV"
                title="IGTV"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-comments"
                title="Комментарии"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
              <v-btn
                class="quick-order__button quick-order__button-services quick-order__button-reels"
                title="Reels"
                @click="clickBtn"
                :grey="true"
              >
              </v-btn>
            </div>
            <div class="quick-order__list-button-order">
              <v-btn
                class="quick-order__button-order"
                title="Оформить  заказ"
                @click="clickBtn"
                :orange="true"
              >
              </v-btn>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="feedback-customer">
    <div class="container">
      <div class="feedback-customer__inner">
        <div class="feedback-customer__title-buttons-wrapper">
          <h2 class="feedback-customer__title">Отзывы клиентов</h2>
        </div>
        <div class="feedback-customer__items">
          <Feedback></Feedback>
          <Feedback></Feedback>
          <Feedback></Feedback>
        </div>
      </div>
    </div>
  </div>
  <section class="stages">
    <div class="container">
      <div class="stages__inner">
        <h2 class="stages__title">Как работает SMM<span>Flow</span></h2>
        <div class="stages__items">
          <StagesItem />
        </div>
      </div>
    </div>
  </section>
  <section class="advantages">
    <div class="container">
      <div class="advantages__inner">
        <h2 class="advantages__title">Преимущества</h2>
        <div class="advantages__items">
          <advantagesItem
            title="Другие сайты"
            item1="1-2%"
            item2="95% успеха"
            item3="Высокая"
            item4="> 1000"
          >
          </advantagesItem>
          <advantagesItem
            image="src/assets/svg/logo.svg"
            :orange="true"
            item1="1-2%"
            item2="95% успеха"
            item3="Высокая"
            item4="> 1000"
          >
          </advantagesItem>
          <advantagesItem
            title="Накрутка"
            item1="1-2%"
            item2="95% успеха"
            item3="Высокая"
            item4="> 1000"
          >
          </advantagesItem>
          <advantagesItem
            title="Официальная реклама"
            item1="1-2%"
            item2="95% успеха"
            item3="Высокая"
            item4="> 1000"
          >
          </advantagesItem>
        </div>
      </div>
    </div>
  </section>
  <section class="faq">
    <div class="container">
      <div class="faq__inner">
        <h2 class="faq__title">Частые вопросы</h2>
        <div class="faq__items">
          <FaqQuestion />
        </div>
      </div>
    </div>
  </section>
  <div class="banner">
    <div class="container">
      <div class="banner__inner">
        <div class="banner__block-text">
          <h2 class="banner__title">
            Закажите больше активности в ваших социальных сетях
          </h2>
          <v-btn
            class="banner__button"
            title="Начать продвижение"
            @click="clickBtn"
            :orange="true"
          >
          </v-btn>
        </div>
        <div class="banner__block-social"></div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
</style>