<template>
  <header class="header">
    <div class="container">
      <div class="header__inner" :class="this.showMobileMenu ? 'active' : ''">
        <div class="header__logo">
          <NuxtLink to="/"
            ><img src="../public/img/icons/logo.png" alt="Logo"
          /></NuxtLink>
        </div>
        <nav
          class="header__menu menu"
          :class="this.showMobileMenu ? 'active' : ''"
        >
          <ul class="menu__list">
            <li
              class="menu__list-item"
              v-for="(item, index) in menuList"
              :key="index"
            >
              <NuxtLink class="menu__list-item-link" :to="item.path">{{
                item.name
              }}</NuxtLink>
            </li>
          </ul>
          <div class="header__buttons">
            <v-btn
              class="header__button"
              title="Войти"
              :headerButton="true"
              :white="true"
              :class="this.isActive ? 'active' : ''"
              @click="loginButton()"
            >
            </v-btn>
            <v-btn
              class="header__button"
              title="Быстрый заказ"
              @click="clickBtn"
              :headerButton="true"
              :orange="true"
            >
            </v-btn>
          </div>
        </nav>
        <nav
          class="header__burger"
          :class="this.showMobileMenu ? 'active' : ''"
          @click="showMenu()"
        >
          <span></span>
        </nav>
      </div>
    </div>
  </header>
</template>



<script>
import vBtn from "./AppButton.vue";

export default {
  name: "TheHeader",
  components: {
    vBtn,
  },
  data() {
    return {
      menuList: [
        {
          name: "Услуги",
          path: "/services",
        },
        {
          name: "Отзывы",
          path: "/reviews",
        },
        {
          name: "Как это работает",
          path: "/howitworks",
        },
        {
          name: "Преимущества",
          path: "/advantages",
        },
        {
          name: "Частые вопросы",
          path: "/questions",
        },
      ],
      showMobileMenu: false,
      isActive:false
    };
  },
  methods: {
    showMenu() {
      this.showMobileMenu = !this.showMobileMenu;
      document.querySelector("body").classList.toggle("_lock");
    },
    loginButton() {
      this.isActive = !this.isActive;
      document.querySelector("body").classList.toggle("_lock");
      document.querySelector('.popup').classList.add('active')
    }
  },
};
</script>



<style scoped lang="scss">
.header {
  @media (max-width: 1099.98px) {
    &__burger {
      z-index: 6;
      position: absolute;
      width: 30px;
      right: 5%;
      height: 21px;
      cursor: pointer;
    }

    &__burger span {
      position: absolute;
      background-color: #ff6e30;
      width: 100%;
      height: 3px;
      right: 0;
      top: 9px;
      transition: 0.3s cubic-bezier(0.8, 0.5, 0.2, 1.4);
    }

    &__burger::before,
    &__burger::after {
      position: absolute;
      content: "";
      background-color: #ff6e30;
      width: 100%;
      height: 3px;
      right: 0;
      transition: 0.3s cubic-bezier(0.8, 0.5, 0.2, 1.4);
    }

    &__burger::before {
      top: 0;
    }

    &__burger::after {
      bottom: 0;
    }

    &__burger.active:before {
      left: 3px;
      top: 12px;
      width: 30px;
      transition: 0.3s cubic-bezier(0.8, 0.5, 0.2, 1.4);
      transform: rotate(90deg);
      transition-delay: 150ms;
    }

    &__burger.active:after {
      left: 14px;
      top: 20px;
      width: 20px;
      transition: 0.3s cubic-bezier(0.8, 0.5, 0.2, 1.4);
      transform: rotate(-45deg);
      transition-delay: 100ms;
    }

    &__burger.active span {
      left: 2px;
      top: 20px;
      width: 20px;
      transition: 0.3s cubic-bezier(0.8, 0.5, 0.2, 1.4);
      transform: rotate(45deg);
      transition-delay: 50ms;
    }

    &__menu.active {
      transform: translate(0);
    }

    &__menu {
      position: fixed;
      height: 100%;
      top: 0;
      left: 0;
      z-index: 5;
      padding: 90px 0 0 0;
      flex-direction: column;
      justify-content: space-between;
      overflow: auto;
      background: #1e252b;
      transition: all 0.4s cubic-bezier(0.22, 0.61, 0.36, 1);
      transform: translate(-100%);
    }

    &__menu.menu.active:before {
      position: absolute;
      background-color: #283036;
      content: "";
      width: 100%;
      height: 1px;
      top: 9.2rem;
      left: 0;
    }
  }
  &__inner {
    min-height: 9.2rem;
    display: flex;
    align-items: center;
  }
  &__logo {
    max-width: 14.654rem;
    width: 100%;
    @media (max-width: 1099.98px) {
      position: relative;
      z-index: 6;
    }
  }
  &__menu {
    display: flex;
    align-items: center;
    width: 100%;
  }
  &__buttons {
    display: flex;
    gap: 1.6rem;
    @media (max-width: 1099.98px) {
      margin-bottom: 2rem;
    }
  }
  &__button {
    padding: 1.3rem 2rem;
    white-space: nowrap;
  }
  &__btn-login {
    font-family: "Nunito Sans";
    font-style: normal;
    font-weight: 400;
    font-size: 1.6rem;
    line-height: 160%;
    display: flex;
    align-items: center;
    color: #ffffff;
  }
}
.menu {
  &__list {
    display: flex;
    align-items: center;
    width: 100%;
    @media (max-width: 1099.98px) {
      flex-direction: column;
      margin: 0 auto;
    }
  }
  &__list-item {
    @media (max-width: 1099.98px) {
      width: 100%;
    }
    &:not(:last-child) {
      margin-right: 2.8rem;
      @media (max-width: 1099.98px) {
        margin: 0;
      }
    }
  }
  &__list-item-link {
    font-family: "Nunito Sans";
    font-style: normal;
    font-weight: 400;
    font-size: 1.6rem;
    line-height: 160%;
    display: flex;
    align-items: center;
    color: #212121;
    transition-duration: 0.15s;
    &:hover {
      color: #FF772D;
    }
    @media (max-width: 1099.98px) {
      color: #ffffff;
      width: 100%;
      justify-content: center;
      padding: 1.5rem 0;
      transition-duration: 0.15s;
      &:hover {
        background: #283036;
      }
    }
  }
}
</style>