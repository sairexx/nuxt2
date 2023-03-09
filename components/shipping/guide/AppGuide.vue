<template>
  <section class="guide">
    <div class="guide__wrapper">
      <img
        class="guide__background"
        src="~/assets/images/shipping/guide-background.png"
        alt=""
      />
      <div class="guide__container">
        <h2 class="guide__title">как купить?</h2>
        <div class="guide__content">
          <div class="guide__content-header">
            <div class="guide__case">
              <div class="guide__case-header">
                <img
                  class="guide__case-icon"
                  src="~/assets/icons/shipping-star.svg"
                  alt=""
                /><span class="guide__content-title">частному покупателю</span>
              </div>
              <div class="guide__case-info">
                <span class="guide__content-text"
                  >Наличный расчет при самовывозе товара со склада нашей
                  компании;</span
                ><span class="guide__content-text"
                  >Оплата в почтовом отделении или транспортной компании при
                  получении товара;</span
                ><span class="guide__content-text"
                  >Оплата на карту Сбербанк через систему «Сбербанк Онлайн» или
                  банкомат.</span
                >
              </div>
            </div>
            <div class="guide__case">
              <div class="guide__case-header">
                <img
                  class="guide__case-icon"
                  src="~/assets/icons/shipping-star.svg"
                  alt=""
                /><span class="guide__content-title"
                  >организации (ооо, ип, кфх)</span
                >
              </div>
              <div class="guide__case-info">
                <span class="guide__content-text"
                  >Безналичная оплата на расчетный счет нашей компании.</span
                >
              </div>
            </div>
          </div>
          <div class="guide__content-footer">
            <span class="guide__content-title"
              >также возможна оплата наложенным платежом</span
            >
            <div class="guide__content-list">
              <span class="guide__content-text">Мы отправляем Вам товар.</span
              ><span class="guide__content-text"
                >Груз прибывает в место назначения.</span
              ><span class="guide__content-text"
                >Вы проверяете груз, убеждаетесь, что все в порядке, и только
                потом производите оплату.</span
              >
            </div>
          </div>
        </div>
        <div class="guide__payments">
          <img
            class="guide__payments-icon guide__payments-icon_master"
            src="~/assets/icons/shipping-mastercard.svg"
            alt=""
          /><img
            class="guide__payments-icon guide__payments-icon_visa"
            src="~/assets/icons/shipping-visa.svg"
            alt=""
          /><img
            class="guide__payments-icon guide__payments-icon_mir"
            src="~/assets/icons/shipping-mir.svg"
            alt=""
          /><img
            class="guide__payments-icon guide__payments-icon_sber"
            src="~/assets/icons/shipping-sber.svg"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppGuide",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.guide {
  display: flex;
  justify-content: center;

  width: 100%;

  &__background {
    display: none;

    @include ut.tablet {
      display: block;
      position: absolute;
      right: 0;
      width: 547.06px;
      height: 778.04px;
      margin: -51px -102px 0 0px;
    }

    @include ut.desktop {
      width: 712px;
      height: 998.04px;
      margin: -61px -1px 0px 0px;
    }
  }

  &__wrapper {
    display: flex;
    justify-content: center;
    width: 100%;

    padding: 70px 29px 162px 24px;

    @include ut.tablet {
      position: relative;
      overflow: hidden;

      padding: 52px 29px 36px 24px;
    }

    @include ut.desktop {
      padding: 74px 29px 54px 24px;
    }

    max-width: 1440px;
    background: #0020d0;
  }

  &__container {
    display: flex;
    flex-direction: column;
    gap: 47px;

    width: 100%;
    max-width: 788px;

    @include ut.tablet {
      gap: 49px;
    }

    @include ut.desktop {
      gap: 45px;
      max-width: 1229px;
    }
  }

  &__title {
    margin-left: 15px;

    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 23px;

    text-transform: uppercase;

    color: #ffffff;

    @include ut.tablet {
      font-size: 24px;
      line-height: 29px;
    }

    @include ut.desktop {
      font-size: 40px;
      line-height: 58px;

      margin-left: 26px;
    }
  }

  &__content {
    display: flex;
    flex-direction: column;
    gap: 32px;

    @include ut.tablet {
      gap: 20px;
    }

    @include ut.desktop {
      gap: 49px;
    }

    &-header {
      display: flex;
      flex-direction: column;
      align-self: flex-start;

      gap: 36px;

      @include ut.tablet {
        gap: 30px;
      }

      @include ut.desktop {
        gap: 40px;
      }
    }

    &-footer {
      display: flex;
      flex-direction: column;
      gap: 13px;

      padding: 22px 10px 19px 13px;

      border-radius: 30px;
      border: 2px solid #ffffff;

      max-width: 404px;

      @include ut.tablet {
        gap: 22px;
        padding: 26px 17px 33px 12px;

        .guide__content-title {
          max-width: 390px;
        }
      }

      @include ut.desktop {
        gap: 14px;
        padding: 40px 17px 43px 27px;
        max-width: 627px;

        .guide__content-title {
          max-width: 481px;
        }
      }
    }

    &-title {
      // font-family: vars.$druk-wide;
      font-style: normal;
      font-weight: 700;
      font-size: 15px;
      line-height: 19px;

      text-transform: uppercase;

      color: #ffffff;

      @include ut.tablet {
        font-family: vars.$druk-cyr;
        font-size: 16px;
        max-width: 293px;
      }

      @include ut.desktop {
        font-size: 22px;
        line-height: 27px;

        max-width: 500px;
      }
    }

    &-list {
      display: flex;
      flex-direction: column;

      gap: 10px;
    }

    &-text {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #ffffff;

      @include ut.desktop {
        line-height: 24px;
      }

      @include ut.desktop {
        font-size: 18px;
        line-height: 24px;
      }
    }
  }

  &__payments {
    display: flex;

    padding-left: 18px;
    margin: -5px 0 0 0;

    @include ut.tablet {
      margin: -16px 0 0 0;
    }
    @include ut.desktop {
      margin: -2px 0 0px -20px;
    }

    &-icon {
      max-width: 100px;

      @include ut.desktop {
        max-width: unset;
      }

      &_master {
        @include ut.desktop {
          width: 168px;
        }
      }

      &_visa {
        margin: 0 0 0 5px;

        @include ut.tablet {
          width: 55.41px;

          margin: 0 0 0 13px;
        }
        @include ut.desktop {
          width: 84px;

          margin: 0 0 0 5px;
        }
      }

      &_mir {
        margin: 0 0 0 22px;

        @include ut.tablet {
          width: 76px;

          margin: 0 0 0 24px;
        }
        @include ut.desktop {
          width: 111px;

          margin: 0 0 0 36px;
        }
      }

      &_sber {
        margin: 0 0 0 17px;

        @include ut.tablet {
          width: 84px;

          margin: 0 0 0 18px;
        }

        @include ut.desktop {
          width: 123px;

          margin: 0 0 0 28px;
        }
      }
    }
  }

  &__case {
    display: flex;
    flex-direction: column;
    gap: 4px;
    margin-left: 25px;
    flex: 0 0 auto;

    &:last-child {
      gap: 12px;

      @include ut.desktop {
        gap: 3px;
      }

      .guide__case-description {
        gap: 5px;
      }

      .guide__content-text {
        width: 290px;

        @include ut.tablet {
          width: 361px;
        }

        @include ut.desktop {
          width: 616px;
        }
      }
    }

    @include ut.tablet {
      justify-content: flex-start;
      margin-left: 0;
      gap: 17px;
    }

    @include ut.desktop {
      gap: 8px;
    }

    &-header {
      display: flex;
      align-items: center;
      gap: 20px;

      @include ut.tablet {
        gap: 8px;
      }

      @include ut.desktop {
        gap: 10px;
      }
    }

    &-icon {
      width: 30px;
      height: 30px;

      margin-top: -5px;

      @include ut.desktop {
        width: 55px;
        height: 55px;
      }
    }

    &-description {
      display: flex;
      flex-direction: column;
      gap: 8px;

      margin-top: 5px;
    }

    &-info {
      display: flex;
      flex-direction: column;

      gap: 10px;

      padding-left: 50px;

      @include ut.tablet {
        max-width: 422px;
        margin-left: -36px;
      }

      @include ut.desktop {
        margin-left: -23px;
        max-width: 622px;
      }
    }
  }
}
</style>
