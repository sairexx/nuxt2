<template>
  <section class="about">
    <div class="about__container">
      <div class="about__wrapper">
        <h2 class="about__title">о компании</h2>
        <span class="about__text"
          >ООО «НПК «Стамакс» — российский завод-изготовитель электропастухов. С
          2013 года производим и продаем электропастухи «Статик-3М». в Барнауле.
          Гарантируем лучшие цены и быстрое сервисное обслуживание</span
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppAbout",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.about {
  display: flex;
  justify-content: center;

  width: 100%;

  &__container {
    display: flex;
    justify-content: flex-start;
    align-items: flex-end;
    width: 100%;
    height: 864px;

    background-size: cover;
    background-repeat: no-repeat;
    background-image: url("~/assets/images/about/about-background-mobile.png");

    @include ut.tablet {
      height: 621px;
      background-image: url("~/assets/images/about/about-background-tablet.png");
    }

    @include ut.desktop {
      max-width: 1440px;
      height: 932px;
      background-image: url("~/assets/images/about/about-background-desktop.png");
    }
  }

  &__wrapper {
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    gap: 15px;

    padding: 0 39px 42px 39px;

    width: 100%;
    height: 367px;

    max-width: 544px;
    background-repeat: no-repeat;
    background-position: center;
    background-image: url("~/assets//images/about/about-wrapper-mobile.png");

    @include ut.tablet {
      max-width: unset;
      width: 723.2px;
      height: 416.98px;

      gap: 24px;
      padding: 0 39px 53px 130px;
      background-image: url("~/assets//images/about/about-wrapper-tablet.png");
    }

    @include ut.desktop {
      padding: 0 39px 79px 130px;

      width: 1017px;
      height: 625.81px;

      background-image: url("~/assets//images/about/about-wrapper-desktop.png");
    }
  }

  &__title {
    font-style: normal;
    font-weight: 500;
    font-size: 24px;
    line-height: 31px;
    text-transform: uppercase;

    color: #ffffff;

    @include ut.desktop {
      font-size: 40px;
      line-height: 58px;
    }
  }

  &__text {
    max-width: 350px;

    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 15px;
    line-height: 19px;

    color: #ffffff;

    @include ut.tablet {
      max-width: 505px;

      font-size: 18px;
      line-height: 23px;
    }

    @include ut.desktop {
      max-width: 580px;

      font-size: 24px;
      line-height: 29px;
    }
  }
}
</style>
