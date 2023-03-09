<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__info">
        <img class="footer__logo" src="~/assets/images/logo.svg" alt="" /><span
          class="footer__license footer__license_tablet"
          >2013–2022 © ООО «НПК «Стамакс» Электропастух СТАТИК-3м</span
        >
      </div>
      <div class="footer__contacts">
        <div class="footer__links">
          <a class="footer__number" href="tel: +88005500485">8-800-550-04-85</a>
          <div class="footer__controls">
            <button class="footer__button">
              <a class="footer__button-link" href=""></a
              ><span class="footer__button-text">vk</span>
            </button>
            <button class="footer__button">
              <a class="footer__button-link" href=""></a
              ><span class="footer__button-text">ok</span>
            </button>
          </div>
        </div>
        <span class="footer__license footer__license_mobile"
          >2013–2022 © ООО «НПК «Стамакс» Электропастух СТАТИК-3м</span
        >
        <div class="footer__design">
          <span class="footer__design-text">Дизайн сайта:</span
          ><img
            class="footer__design-image"
            src="~/assets/images/design-logo.svg"
            alt=""
          />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.footer {
  display: flex;
  justify-content: center;
  width: 100%;

  flex: 0 1 auto;
  background: #2c2c2c;

  &__container {
    display: flex;
    flex-direction: column;
    width: 100%;

    padding: 29px 0px 22px 39px;
    gap: 15px;

    @include ut.tablet {
      padding: 27px 0 23px 0;
      width: 764px;

      flex-direction: row;
      justify-content: space-between;
    }

    @include ut.desktop {
      width: 1180px;
      padding: 42px 0 45px 0;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;

    @include ut.tablet {
      gap: 16px;
    }

    @include ut.desktop {
      gap: 22px;
    }
  }

  &__logo {
    width: 110px;
    height: 26px;

    @include ut.tablet {
      height: 33px;
      width: 137px;
    }

    @include ut.desktop {
      height: 44px;
      width: 180px;
    }
  }

  &__license {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    color: #bbbbbb;

    &_tablet {
      display: none;

      @include ut.tablet {
        display: flex;
        width: 250px;
      }

      @include ut.desktop {
        font-size: 16px;
        line-height: 20px;

        color: #bbbbbb;
        width: 300px;
      }
    }

    &_mobile {
      display: flex;
      width: 91%;

      @include ut.tablet {
        display: none;
      }
    }
  }
  &__contacts {
    display: flex;
    flex-direction: column;
    gap: 15px;

    @include ut.tablet {
      margin-right: 26px;
      gap: 38px;
    }

    @include ut.desktop {
      margin-right: 13px;
      margin-top: 4px;
      gap: 48px;
    }
  }

  &__links {
    display: flex;
    align-items: center;
    gap: 16px;

    @include ut.desktop {
      gap: 24px;
    }
  }

  &__number {
    font-family: vars.$montserrat;

    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 20px;
    text-transform: uppercase;

    color: #bbbbbb;

    @include ut.desktop {
      font-size: 18px;
      line-height: 22px;
    }
  }

  &__controls {
    display: flex;
    gap: 7px;

    @include ut.desktop {
      gap: 11px;
    }
  }

  &__button {
    position: relative;

    display: flex;
    align-items: center;
    justify-content: center;

    width: 28px;
    height: 28px;

    border: none;
    outline: none;
    border-radius: 50%;

    background: #0020d0;

    @include ut.desktop {
      width: 37px;
      height: 37px;
    }

    &:active {
      .footer__button-text {
        color: #ffffff;
      }
    }
    &:hover {
      .footer__button-text {
        color: #ffffff;
      }
    }

    &-link {
      position: absolute;
      top: 0;
      left: 0;

      width: 100%;
      height: 100%;
    }

    &-text {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 700;
      font-size: 12px;
      line-height: 15px;
      text-transform: uppercase;

      color: #bbbbbb;

      @include ut.desktop {
        font-size: 15px;
        line-height: 18px;
      }
    }
  }

  &__design {
    display: flex;
    align-items: center;
    gap: 11px;

    @include ut.desktop {
      gap: 5px;
    }

    &-text {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #bbbbbb;

      @include ut.desktop {
        font-size: 16px;
        line-height: 20px;
      }
    }

    &-image {
      width: 85px;
      height: 11px;

      @include ut.desktop {
        height: 12px;
        width: 99px;
        margin: 4px 0 0 0;
      }
    }
  }
}
</style>
