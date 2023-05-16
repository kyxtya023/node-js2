<template>
  <section class="services">
    <div class="container">
      <div class="services__inner">
        <ul class="services__list" v-for="item in items" :key="item.name">
          <div class="services__list-img-name">
            <img
              class="services__list-img"
              :src="item.img"
              :alt="item.altImg"
            />
            <h4 class="services__list-name">{{ item.name }}</h4>
          </div>
          <li
            class="services__list-item"
            v-for="listItem in item.list"
            :key="listItem"
          >
            <router-link to="/" class="services__list-item-link">{{
              listItem
            }}</router-link>
          </li>
        </ul>
      </div>
    </div>
  </section>
  <div class="popup active" id="popup-2" data-popup>
    <div class="popup__wrapper">
      <div class="popup__inner">
        <div class="popup__title">Вход в аккаунт</div>
        <div class="popup__form-wrapper">
          <div class="popup__form-input-block">label</div>
        </div>
        <button class="popup__button popup__button--close btn" data-popup-close>
          Закрыть
        </button>
      </div>
    </div>
  </div>
  <button
    class="popup__button popup__button--open btn"
    data-popup-button="popup-2"
  >
    Открыть
  </button>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      items: [
        {
          img: "src/assets/img/IconQuickOrderInstagram.png",
          altImg: "Instagram",
          name: "Instagram",
          list: [
            "Подписчики",
            "Лайки",
            "Просмотры",
            "Комментарии",
            "Истории",
            "Зрители",
            "Статистика",
          ],
        },
        {
          img: "src/assets/img/IconQuickOrderTelegram.png",
          altImg: "Telegram",
          name: "Telegram",
          list: [
            "Подписчики",
            "Просмотры",
            "Реакции",
            "Голосование",
            "Репосты",
            "Старт бота",
            "Telegraph просмотры",
            "Комментарии",
          ],
        },
        {
          img: "src/assets/img/IconQuickOrderVK.png",
          altImg: "VK",
          name: "VK",
          list: [
            "Подписчики",
            "Лайки",
            "Комментарии",
            "Репосты",
            "Просмотры на видео",
            "Просмотры на пост",
            "Накрутка опросов",
            "Прослушивания",
            "Релиз плейлиста",
          ],
        },
        {
          img: "src/assets/img/IconQuickOrderTikTok.png",
          altImg: "TikTok",
          name: "TikTok",
          list: ["Подписчики", "Лайки", "Комментарии", "Репосты", "Просмотры"],
        },
        {
          img: "src/assets/img/IconQuickOrderYouTube.png",
          altImg: "YouTube",
          name: "YouTube",
          list: [
            "Подписчики",
            "Просмотры",
            "Просмотры трансляций",
            "Просмотры Shorts",
            "Лайки",
            "Дизлайки",
            "Комментарии",
            "Репосты",
            "Часы просмотров",
          ],
        },
        {
          img: "src/assets/img/IconQuickOrderTwitch.png",
          altImg: "Twitch",
          name: "Twitch",
          list: ["Просмотры", "Подписчики", "Зрители"],
        },
        {
          img: "src/assets/img/IconQuickOrderFacebook.png",
          altImg: "Facebook",
          name: "Facebook",
          list: [
            "Подписчики",
            "Лайки",
            "Просмотры",
            "Комментарии",
            "Истории",
            "Зрители",
            "Статистика",
          ],
        },
        {
          img: "src/assets/img/IconQuickOrderTwitter.png",
          altImg: "Twitter",
          name: "Twitter",
          list: [
            "Подписчики",
            "Лайки",
            "Просмотры",
            "Комментарии",
            "Репосты",
            "Просмотры на видео",
            "Просмотры на пост",
            "Накрутка опросов",
            "Прослушивания",
            "Релиз плейлиста",
          ],
        },
        {
          img: "src/assets/img/IconQuickOrderRuTube.png",
          altImg: "RuTube",
          name: "RuTube",
          list: ["Подписчики", "Лайки", "Комментарии", "Репосты", "Просмотры"],
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
</style>