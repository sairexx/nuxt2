<template>
  <section class="advantages">
    <div class="advantages__wrapper">
      <div class="advantages__container">
        <h2 class="advantages__title">почему мы?</h2>
        <div class="advantages__list">
          <div class="advantages__item">
            <div class="advantages__item-header">
              <div class="advantages__item-icon">
                <img
                  class="advantages__item-icon-source"
                  src="~/assets/icons/advantages-building.svg"
                  alt=""
                />
              </div>
              <span class="advantages__item-title">>270 000 Га</span>
            </div>
            <span class="advantages__item-text"
              >огорожено за 7 лет с начала производства электропастухов</span
            >
          </div>
          <div class="advantages__item">
            <div class="advantages__item-header">
              <div class="advantages__item-icon">
                <img
                  class="advantages__item-icon-source"
                  src="~/assets/icons/advantages-animal.svg"
                  alt=""
                />
              </div>
              <span class="advantages__item-title">>7 000</span>
            </div>
            <span class="advantages__item-text"
              >российских и зарубежных хозяйств выбрали Статик-3М</span
            >
          </div>
          <div class="advantages__item">
            <div class="advantages__item-header">
              <div class="advantages__item-icon">
                <img
                  class="advantages__item-icon-source"
                  src="~/assets/icons/advantages-achievement.svg"
                  alt=""
                />
              </div>
              <span class="advantages__item-title">18 месяцев</span>
            </div>
            <span class="advantages__item-text"
              >составляет гарантийный срок обслуживания каждого прибора</span
            >
          </div>
          <div class="advantages__item advantages__item_flag">
            <div class="advantages__item-header">
              <div class="advantages__item-icon">
                <img
                  class="advantages__item-icon-source"
                  src="~/assets/icons/advantages-flag.svg"
                  alt=""
                />
              </div>
              <span class="advantages__item-title">производим в России</span>
            </div>
            <span class="advantages__item-text"
              >Мы находимся в Алтайском крае — крупном аграрном регионе. Поэтому
              не понаслышке знаем об особенностях содержания скота</span
            >
          </div>
          <div class="advantages__item advantages__item_wallet">
            <div class="advantages__item-header">
              <div class="advantages__item-icon">
                <img
                  class="advantages__item-icon-source"
                  src="~/assets/icons/advantages-wallet.svg"
                  alt=""
                />
              </div>
              <span class="advantages__item-title"
                >Оплата наложенным платежом</span
              >
            </div>
            <span class="advantages__item-text"
              >Отправляем заказы наложенным платежом. Оплата происходит при
              получении товара лично в руки</span
            >
          </div>
          <div class="advantages__item advantages__item_delivery">
            <div class="advantages__item-header">
              <div class="advantages__item-icon">
                <img
                  class="advantages__item-icon-source"
                  src="~/assets/icons/advantages-delivery.svg"
                  alt=""
                />
              </div>
              <span class="advantages__item-title"
                >Доставка в любой населенный пункт</span
              >
            </div>
            <span class="advantages__item-text"
              >Высылаем электропастухи во все населенные пункты России и
              ближнего зарубежья</span
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppAdvantages",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.advantages {
  display: flex;
  justify-content: center;

  width: 100%;

  &__wrapper {
    display: flex;
    justify-content: center;
    background: #0020d0;

    width: 100%;
    max-width: 1440px;
  }

  &__container {
    display: flex;
    flex-direction: column;
    gap: 45px;

    width: 100%;
    max-width: 768px;

    padding: 70px 39px 79px 39px;

    @include ut.tablet {
      padding: 37px 0 36px 0;
    }

    @include ut.desktop {
      gap: 79px;
      padding: 79px 0 85px 0;

      max-width: 1174px;
    }
  }

  &__title {
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 23px;
    text-transform: uppercase;

    color: #ffffff;

    @include ut.tablet {
      font-size: 24px;
      line-height: 31px;
    }

    @include ut.desktop {
      font-size: 40px;
      line-height: 49px;
    }
  }

  &__list {
    display: flex;
    flex-wrap: wrap;

    gap: 44px;

    padding: 0 0 0 11px;

    @include ut.tablet {
      padding: 0;

      row-gap: 58px;
      column-gap: 16px;
    }

    @include ut.desktop {
      row-gap: 87px;
      column-gap: 58px;
    }
  }

  &__item {
    display: flex;
    flex-direction: column;
    gap: 7.5px;

    @include ut.tablet {
      gap: 13.5px;
      width: 100%;
      max-width: 245px;
    }

    @include ut.desktop {
      max-width: 342px;
      gap: 21.5px;
    }

    &_flag {
      @include ut.tablet {
        gap: 53px;

        .advantages__item-header {
          gap: 17px;
        }

        .advantages__item-title {
          max-width: 190px;
        }
      }

      @include ut.desktop {
        max-width: 382px;

        gap: 52px;

        .advantages__item-header {
          gap: 31px;
        }
      }
    }

    &_wallet {
      @include ut.tablet {
        .advantages__item-header {
          gap: 14px;
        }

        gap: 32px;
      }

      @include ut.desktop {
        margin-left: -39px;
        gap: 23px;

        .advantages__item-header {
          gap: 28px;
        }
      }
    }

    &_delivery {
      @include ut.tablet {
        .advantages__item-header {
          gap: 14px;
        }

        gap: 11px;
      }

      @include ut.desktop {
        .advantages__item-header {
          gap: 30px;
        }

        max-width: 348px;
        margin-left: -2px;
        gap: 51px;
      }
    }

    &-header {
      display: flex;
      align-items: center;
      gap: 18px;

      @include ut.tablet {
        gap: 7px;
        align-items: flex-start;
        flex-direction: column;
      }

      @include ut.desktop {
        gap: 18px;
      }
    }

    &-icon {
      display: flex;
      align-items: center;
      justify-content: center;
      max-width: 29px;

      @include ut.tablet {
        max-width: 50px;
        max-height: 33px;
      }

      &-source {
        width: 100%;
        height: 100%;
      }
    }

    &-title {
      font-weight: 700;
      font-size: 15px;
      line-height: 19px;
      text-transform: uppercase;

      color: #ffffff;

      @include ut.tablet {
        font-size: 16px;
        line-height: 21px;
      }

      @include ut.desktop {
        font-size: 22px;
        line-height: 28px;
      }
    }

    &-text {
      padding-left: 49px;

      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #ffffff;

      @include ut.tablet {
        padding: 0;
      }

      @include ut.desktop {
        font-size: 18px;
        line-height: 26px;
      }
    }
  }
}
</style>
