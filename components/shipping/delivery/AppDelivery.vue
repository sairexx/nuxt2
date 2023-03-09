<template>
  <section class="shipping">
    <div class="shipping__container">
      <div class="shipping__head">
        <img
          class="shipping__image"
          src="~/assets/images/shipping/shipping-image.png"
          alt=""
        />
        <div class="shipping__info">
          <h2 class="shipping__title">доставка</h2>
          <div class="shipping__description">
            <span class="shipping__text"
              >Отправляем заказанный товар во все регионы России, включая
              Калининградскую область и Крым.</span
            ><span class="shipping__text"
              >Продукция сертифицирована на территории стран Таможенного союза,
              поэтому возможна доставка в Казахстан, Белоруссию, Армению,
              Киргизию.</span
            >
          </div>
        </div>
      </div>
      <div class="shipping__list">
        <div class="shipping__item shipping__item_delivery">
          <div class="shipping__item-head">
            <img
              class="shipping__item-icon"
              src="~/assets/icons/shipping-delivery.svg"
              alt=""
            />
            <h3 class="shipping__item-title">Транспортной компанией</h3>
          </div>
          <div class="shipping__item-text">
            Мы работаем со всеми основными грузоперевозчиками, которые есть во
            всех городах и многих районных центрах. Транспортная компания
            доставляет до ближайшего к Вам пункта выдачи груза. Возможен любой
            вес и объем.
          </div>
        </div>
        <div class="shipping__item shipping__item_post">
          <div class="shipping__item-head">
            <img
              class="shipping__item-icon"
              src="~/assets/icons/shipping-post.svg"
              alt=""
            />
            <h3 class="shipping__item-title">Почтой России</h3>
          </div>
          <div class="shipping__item-text">
            Отправляем посылки весом до 20 кг. Посылки большего веса и стойки
            для проволоки Почта России не принимает.
          </div>
        </div>
        <div class="shipping__item shipping__item_bus">
          <div class="shipping__item-head">
            <img
              class="shipping__item-icon"
              src="~/assets/icons/shipping-bus.svg"
              alt=""
            />
            <h3 class="shipping__item-title">междугородним автобусом</h3>
          </div>
          <div class="shipping__item-text">
            В пределах 300 км от Барнаула возможна отправка груза междугородним
            автобусом с Барнаульского автовокзала. Наш экспедитор доставит товар
            «до дверей». По договоренности мы отправляем другими способами, если
            это возможно.
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppDelivery",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.shipping {
  display: flex;
  justify-content: center;

  width: 100%;

  padding: 0 39px 57px 39px;
  margin-top: -151px;

  @include ut.tablet {
    margin-top: 0;

    padding: 0 39px 69px 39px;
  }

  @include ut.desktop {
    padding: 0 39px 188px 39px;
  }

  &__container {
    display: flex;
    flex-direction: column;

    max-width: 765px;
    gap: 39px;

    @include ut.tablet {
      gap: 15px;
    }

    @include ut.desktop {
      padding-top: 97px; //delete

      width: 100%;
      max-width: 1180px;

      gap: 22px;
    }
  }

  &__head {
    display: flex;
    align-items: center;
    flex-direction: column;

    @include ut.tablet {
      align-items: unset;
      flex-direction: row;

      gap: 23px;
    }

    @include ut.desktop {
      gap: 10px;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;
    gap: 10px;

    @include ut.tablet {
      padding: 60px 0 0 0;
      order: 1;

      gap: 21px;
      max-width: 380px;
    }

    @include ut.desktop {
      gap: 30px;
      max-width: 539px;
    }
  }

  &__title {
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 22px;

    text-transform: uppercase;

    color: #0020d0;

    @include ut.tablet {
      font-size: 24px;
      line-height: 29px;
    }

    @include ut.desktop {
      font-size: 40px;
      line-height: 49px;
    }
  }

  &__description {
    display: flex;
    flex-direction: column;

    gap: 10px;
  }

  &__text {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    color: #2c2c2c;

    @include ut.desktop {
      line-height: 24px;
      font-size: 18px;
    }
  }

  &__image {
    width: 351px;
    margin-left: -25px;

    @include ut.tablet {
      align-self: center;

      order: 2;
      width: 350px;
      margin: 17px 0px 0 0px;
    }

    @include ut.desktop {
      width: 640px;
      margin: -51px 0px 0 0px;
    }
  }

  &__list {
    display: flex;
    flex-direction: column;
    gap: 31px;

    padding-left: 8px;

    @include ut.tablet {
      flex-direction: row;
      gap: 15px;

      padding-left: 0;
    }

    @include ut.desktop {
      gap: 14px;
    }
  }

  &__item {
    display: flex;
    flex-direction: column;
    gap: 12px;

    @include ut.tablet {
      gap: 19px;
    }

    &_delivery {
      @include ut.tablet {
        .shipping__item-icon {
          width: 50px;
        }

        .shipping__item-title {
          width: 245px;
        }
        .shipping__item-text {
          width: 245px;
        }
      }

      @include ut.desktop {
        gap: 34px;

        .shipping__item-icon {
          width: 57px;
        }

        .shipping__item-text {
          width: 386px;
        }
      }
    }

    &_post {
      gap: 9px;

      @include ut.tablet {
        gap: 40px;

        .shipping__item-icon {
          width: 37px;
        }

        .shipping__item-title {
          width: 245px;
        }
        .shipping__item-text {
          width: 245px;
        }
      }

      @include ut.desktop {
        gap: 60px;

        .shipping__item-title {
          width: 312px;
        }

        .shipping__item-head {
          gap: 22px;
        }

        .shipping__item-icon {
          width: 42.5px;
          margin: -2px 0 0 0;
        }

        .shipping__item-text {
          width: 375px;
        }
      }
    }

    &_bus {
      margin-top: -2px;

      .shipping__item-icon {
        width: 50px;

        margin-left: -9px;
      }

      .shipping__item-head {
        gap: 12px;
      }

      @include ut.tablet {
        .shipping__item-icon {
          width: 92.8px;

          margin: 2px 0 0 0;
        }

        .shipping__item-head {
          gap: 19px;
        }

        .shipping__item-title {
          width: 245px;
        }
        .shipping__item-text {
          width: 245px;
        }
      }

      @include ut.desktop {
        gap: 33px;
        margin: -1px 0px 0 14px;

        .shipping__item-icon {
          width: 100.8px;
        }

        .shipping__item-head {
          gap: 21px;
        }

        .shipping__item-text {
          width: 380px;
        }
      }
    }

    &-head {
      display: flex;
      align-items: center;
      gap: 17px;

      @include ut.tablet {
        gap: 19px;
        flex-direction: column;
        align-items: flex-start;
      }
    }

    &-icon {
      width: 35px;
    }

    &-title {
      font-style: normal;
      font-weight: 500;
      font-size: 15px;
      line-height: 19px;

      text-transform: uppercase;

      color: #0020d0;

      @include ut.tablet {
        font-size: 16px;
        line-height: 21px;
      }

      @include ut.desktop {
        font-size: 22px;
        line-height: 27px;
      }
    }

    &-text {
      padding-left: 52px;

      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #2c2c2c;

      @include ut.tablet {
        padding-left: 0;
      }

      @include ut.desktop {
        font-size: 18px;
        line-height: 24px;
      }
    }
  }
}
</style>
