<template>
  <section class="info">
    <div class="info__container">
      <div class="info__wrapper">
        <div class="info__item">
          <div class="info__item-head">
            <img
              class="info__item-icon"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
            <h3 class="info__item-title">что такое электропастух?</h3>
          </div>
          <span class="info__item-text"
            >Проволочное ограждение, на которое генератор подает импульсы тока.
            Удар током не вредит животному: он отпугивает и вырабатывает рефлекс
            не приближаться к изгороди. Прибор основан на методических
            рекомендациях НИИ Охраны природы «По применению электроограждений
            для животных»</span
          >
        </div>
        <div class="info__item">
          <div class="info__item-head">
            <img
              class="info__item-icon"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
            <h3 class="info__item-title">как пользоваться электропастухом?</h3>
          </div>
          <span class="info__item-text"
            >В каждую коробку с прибором мы вкладываем подробную инструкцию. По
            ссылке можно посмотреть видеоролик с инструкцией</span
          >
        </div>
        <div class="info__item">
          <div class="info__item-head">
            <img
              class="info__item-icon"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
            <h3 class="info__item-title">безопасность</h3>
          </div>
          <span class="info__item-text"
            >Электропастух безопасен для людей и животных. Удар током не вредит
            здоровью, но это всё равно неприятно. Чтобы никто случайно не задел
            изгородь, все комплекты оснащены предупреждающими знаками</span
          >
        </div>
        <div class="info__item">
          <div class="info__item-head">
            <img
              class="info__item-icon"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
            <h3 class="info__item-title">Технология «Смарт-Шок»</h3>
          </div>
          <span class="info__item-text"
            >Наша умная система автоматически подстраивает мощность генератора
            импульса под конкретную изгородь. Снижено влияние травы. Сила удара
            током одинакова при любом размере ограждения. Удар происходит только
            в том случае, если животное коснулось изгороди</span
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppInfo",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.info {
  position: relative;

  display: flex;
  justify-content: center;

  width: 100%;

  &__container {
    position: relative;

    display: flex;
    justify-content: flex-start;

    width: 100%;

    padding: 64px 0 79px 19px;

    background-size: cover;
    background-repeat: no-repeat;
    background-image: url("~/assets/images/main/info-background-mobile.png");

    @include ut.tablet {
      justify-content: center;
      max-width: 1024px;

      padding: 103px 0 99px 19px;

      background-image: url("~/assets/images/main/info-background-tablet.png");
    }

    @include ut.desktop {
      max-width: 1440px;

      padding: 179px 0 190px 19px;

      backdrop-filter: 20px;
      background-image: url("~/assets/images/main/info-background-desktop.png");
    }
  }

  &__wrapper {
    display: flex;
    flex-wrap: wrap;
    gap: 28px;

    @include ut.tablet {
      column-gap: 59px;
      row-gap: 34px;
      max-width: 822px;
    }

    @include ut.desktop {
      column-gap: 68px;
      row-gap: 50px;
      max-width: 1270px;
    }
  }

  &__item {
    display: flex;
    flex-direction: column;
    gap: 10px;

    @include ut.desktop {
      gap: 23px;
    }

    &-title {
      max-width: 300px;
      margin: 13px 0 2px -27px;

      font-style: normal;
      font-weight: 700;
      font-size: 18px;
      line-height: 23px;
      text-transform: uppercase;

      color: #ffffff;

      @include ut.desktop {
        max-width: 494px;
        margin: 30px 0 2px -51px;

        font-size: 32px;
        line-height: 41px;
      }
    }

    &-icon {
      width: 46px;
      height: 44px;

      @include ut.desktop {
        width: 87px;
        height: 84px;
      }
    }

    &-head {
      display: flex;
    }

    &-text {
      max-width: 368px;
      padding-left: 20px;

      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #ffffff;

      @include ut.tablet {
        max-width: 330px;
      }

      @include ut.desktop {
        padding-left: 36px;

        max-width: 528px;
        font-size: 18px;
        line-height: 26px;
      }
    }
  }
}
</style>
