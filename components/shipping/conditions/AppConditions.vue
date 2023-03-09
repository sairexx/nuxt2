<template>
  <section class="conditions">
    <div class="conditions__wrapper">
      <div class="conditions__container">
        <h2 class="conditions__title">условия доставки</h2>
        <div class="conditions__content">
          <div class="conditions__content-header">
            <div class="conditions__info">
              <span class="conditions__info-title">от 550 рублей</span
              ><span class="conditions__info-subtitle"
                >составляет стоимость доставки.</span
              >
            </div>
            <div class="conditions__info">
              <span class="conditions__info-title">от 2 до 14 дней</span
              ><span class="conditions__info-subtitle"
                >средний срок доставки.</span
              >
            </div>
            <div class="conditions__info">
              <span class="conditions__info-title">в 12:00 мск ежедневно</span
              ><span class="conditions__info-subtitle"
                >заказы отправляются покупателям.</span
              >
            </div>
          </div>
          <div class="conditions__content-footer">
            <span class="conditions__description"
              >Точные стоимость и срок зависят от выбранного способа доставки,
              населенного пункта и размера/веса товара.</span
            ><span class="conditions__description"
              >Наш менеджер подберет наименее затратный способ доставки.</span
            ><span class="conditions__description"
              >О прибытии груза Вас оповестят наш менеджер и оператор
              транспортной компании.</span
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppConditions",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.conditions {
  display: flex;
  justify-content: center;

  width: 100%;
  height: 864px;

  @include ut.tablet {
    padding: 0;
    align-items: flex-start;
    justify-content: center;

    height: 622px;
  }

  @include ut.desktop {
    height: 932px;
  }

  &__wrapper {
    display: flex;
    justify-content: center;
    align-items: flex-end;

    background-image: url("~/assets/images/shipping/shipping-preview.png");

    width: 100%;
    max-width: 1440px;
    height: 864px;

    padding: 0 27px 27px 27px;

    @include ut.tablet {
      height: 622px;
      padding: 0 27px 64px 27px;
    }

    @include ut.desktop {
      align-items: flex-start;
      padding: 55px 0 0 0;
      height: 932px;
    }
  }

  &__container {
    display: flex;
    flex-direction: column;
    gap: 17px;

    width: 100%;
    max-width: 764px;

    @include ut.tablet {
      gap: 37px;
    }

    @include ut.desktop {
      gap: 55px;
      max-width: 1179px;
    }
  }

  &__title {
    margin-left: 12px;

    font-weight: 500;
    font-size: 18px;
    line-height: 22px;
    text-transform: uppercase;

    color: #ffffff;

    @include ut.tablet {
      margin-left: 0;

      font-size: 24px;
      line-height: 29px;
    }

    @include ut.desktop {
      font-size: 40px;
      line-height: 58px;
    }
  }

  &__content {
    display: flex;
    flex-direction: column;
    flex: 0 0 auto;
    gap: 17px;

    width: 100%;
    height: 100%;

    max-width: 375px;
    min-height: 370px;

    padding: 23px 12px 17px 13px;

    border-radius: 30px;
    background: #ffffff;

    @include ut.tablet {
      gap: 20px;
      padding: 33px 12px 45px 16px;
    }

    @include ut.desktop {
      gap: 23px;
      max-width: 380px;
      max-height: 568px;
      padding: 44px 19px 55px 22px;
    }

    &-header {
      display: flex;
      flex-direction: column;
      gap: 15px;

      @include ut.tablet {
        gap: 22px;
      }

      @include ut.desktop {
        gap: 24px;
      }
    }

    &-footer {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;
    gap: 4px;

    @include ut.tablet {
      gap: 7px;
    }

    &:nth-child(2) {
      .conditions__info-subtitle {
        line-height: 17px;
      }
    }

    &-title {
      font-style: normal;
      font-weight: 500;
      font-size: 15px;
      line-height: 18px;
      text-transform: uppercase;

      color: #0020d0;

      @include ut.tablet {
        font-size: 16px;
        line-height: 19px;
      }

      @include ut.desktop {
        font-size: 22px;
        line-height: 27px;
      }
    }

    &-subtitle {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #0020d0;

      @include ut.tablet {
        font-size: 14px;
        line-height: 18px;
      }

      @include ut.desktop {
        font-size: 18px;
        line-height: 24px;
      }
    }
  }

  &__description {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    color: #2c2c2c;

    @include ut.desktop {
      font-size: 16px;
      line-height: 21px;
    }
  }
}
</style>
