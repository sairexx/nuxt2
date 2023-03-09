<template>
  <section class="shop">
    <div class="shop__breadcrumbs">
      <span class="shop__breadcrumbs-text">Каталог</span
      ><img
        class="shop__breadcrumbs-icon"
        src="~/assets/icons/chevron-right.svg"
        alt=""
      /><span class="shop__breadcrumbs-text"
        >Генератор импульсов Статик-3М</span
      >
    </div>
    <div class="shop__container">
      <h2 class="shop__title">комплектующие</h2>
      <div class="shop__grid">
        <div class="shop__filter">
          <span class="shop__filter-title">фильтр</span>
          <div class="shop__filter-list">
            <div class="shop__filter-row">
              <div class="checkbox">
                <label class="checkbox__label" for="checkbox-first"></label>
                <input
                  class="checkbox__input"
                  name="checkbox-first"
                  id="checkbox-first"
                  type="checkbox"
                />
                <div class="checkbox__box">
                  <div class="checkbox__inner"></div>
                </div>
                <span class="checkbox__text">Собственное производство </span>
              </div>
            </div>
            <div class="shop__filter-row">
              <div class="checkbox">
                <label class="checkbox__label" for="checkbox-second"></label>
                <input
                  class="checkbox__input"
                  name="checkbox-second"
                  id="checkbox-second"
                  type="checkbox"
                />
                <div class="checkbox__box">
                  <div class="checkbox__inner"></div>
                </div>
                <span class="checkbox__text">Аксессуары </span>
              </div>
            </div>
            <div class="shop__filter-row">
              <div class="checkbox">
                <label class="checkbox__label" for="checkbox-third"></label>
                <input
                  class="checkbox__input"
                  name="checkbox-third"
                  id="checkbox-third"
                  type="checkbox"
                />
                <div class="checkbox__box">
                  <div class="checkbox__inner"></div>
                </div>
                <span class="checkbox__text">Изгородь </span>
              </div>
            </div>
            <div class="shop__filter-row">
              <div class="checkbox">
                <label class="checkbox__label" for="checkbox-four"></label>
                <input
                  class="checkbox__input"
                  name="checkbox-four"
                  id="checkbox-four"
                  type="checkbox"
                />
                <div class="checkbox__box">
                  <div class="checkbox__inner"></div>
                </div>
                <span class="checkbox__text">Изоляторы </span>
              </div>
            </div>
          </div>
        </div>
        <div class="shop__list">
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-iso-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-iso-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-iso-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title">изолятор для ленты</span
                ><span class="shop__item-subtitle">для ленты любой ширины</span
                ><span class="shop__item-price">25 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-block-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-block-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-block-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title">блок питания</span
                ><span class="shop__item-subtitle">для электропастуха</span
                ><span class="shop__item-price">250 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-acc-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-acc-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-acc-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title"
                  >аккумуляторная батарея для электропастуха</span
                ><span class="shop__item-subtitle"
                  >напряжение 12 В, ёмкость 7 А·ч</span
                ><span class="shop__item-price">1300 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-iso-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-iso-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-iso-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title">изолятор для ленты</span
                ><span class="shop__item-subtitle">для ленты любой ширины</span
                ><span class="shop__item-price">25 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-block-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-block-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-block-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title">блок питания</span
                ><span class="shop__item-subtitle">для электропастуха</span
                ><span class="shop__item-price">250 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item shop__item_disable">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-acc-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-acc-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-acc-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title"
                  >аккумуляторная батарея для электропастуха</span
                ><span class="shop__item-subtitle"
                  >напряжение 12 В, ёмкость 7 А·ч</span
                ><span class="shop__item-price">Нет в продаже</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-shepherd-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-shepherd-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-shepherd-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title"
                  >электропастух для крс на 0,5 га</span
                ><span class="shop__item-subtitle"
                  >300 метров в 2 ряда. Полный комплект</span
                ><span class="shop__item-price">15 190 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-shepherd-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-shepherd-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-shepherd-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title"
                  >электропастух для крс на 1 га</span
                ><span class="shop__item-subtitle"
                  >400 метров в 2 ряда. Полный комплект</span
                ><span class="shop__item-price">16 230 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
          <div class="shop__item">
            <div class="shop__item-image">
              <img
                class="shop__item-image-source shop__item-image-source_mobile"
                src="~/assets/images/shop/shop-shepherd-mobile.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_tablet"
                src="~/assets/images/shop/shop-shepherd-tablet.png"
                alt=""
              /><img
                class="shop__item-image-source shop__item-image-source_desktop"
                src="~/assets/images/shop/shop-shepherd-desktop.png"
                alt=""
              />
            </div>
            <div class="shop__item-info">
              <div class="shop__item-info-wrapper">
                <span class="shop__item-title"
                  >электропастух для крс на 150 га</span
                ><span class="shop__item-subtitle"
                  >5 километров в 2 ряда. Полный комплект</span
                ><span class="shop__item-price">89 420 р</span>
              </div>
              <button class="shop__item-button">
                <span class="shop__item-button-text">в корзину</span>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppShop",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.checkbox {
  position: relative;

  display: flex;
  align-items: center;
  gap: 10px;

  @include ut.tablet {
    align-items: flex-start;
    gap: 15px;
  }

  @include ut.desktop {
    gap: 19px;
  }

  &__label {
    position: absolute;
    top: 0;
    left: 0;

    width: 100%;
    height: 100%;
  }

  &__input {
    display: none;
  }

  .checkbox__input:checked ~ .checkbox__box .checkbox__inner {
    opacity: 1;
    z-index: 2;

    transition: all vars.$transition-duration ease-in-out;
  }

  &__text {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 17px;

    color: #2c2c2c;

    @include ut.tablet {
      font-size: 15px;
      line-height: 18px;
    }

    @include ut.desktop {
      font-size: 16px;
      line-height: 20px;
    }
  }

  &__box {
    display: flex;
    align-items: center;
    justify-content: center;

    flex: 0 0 auto;

    background: #ffffff;
    border: 1px solid #bbbbbb;
    border-radius: 4px;

    width: 20px;
    height: 20px;
  }

  &__inner {
    opacity: 0;
    z-index: -1;

    width: 12px;
    height: 12px;

    border-radius: 3px;

    background-color: rgba(#0020d0, 0.8);
    transition: all vars.$transition-duration ease-in-out;
  }
}

.shop {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 15px;

  width: 100%;
  padding: 19px 39px 60px 39px;

  @include ut.tablet {
    gap: 23px;

    padding: 38px 39px 60px 39px;
  }

  @include ut.desktop {
    padding: 73px 39px 127px 39px;

    gap: 41px;
  }

  &__breadcrumbs {
    display: flex;
    align-items: center;
    gap: 5px;

    width: 100%;
    max-width: 762px;

    @include ut.tablet {
      gap: 8px;
    }

    @include ut.desktop {
      max-width: 1179px;
      gap: 6px;
    }

    &-text {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 29px;

      color: #828282;

      @include ut.tablet {
        font-size: 15px;
      }

      @include ut.desktop {
        font-size: 16px;
        line-height: 29px;
      }
    }

    &-icon {
      width: 4px;
      height: 8px;

      @include ut.tablet {
        width: 8px;
        height: 10px;
      }
    }
  }

  &__container {
    display: flex;
    flex-direction: column;

    width: 100%;

    gap: 20px;
    max-width: 762px;

    @include ut.tablet {
      gap: 29px;
      max-width: 764px;
    }

    @include ut.desktop {
      gap: 50px;
      max-width: 1181px;
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

  &__grid {
    display: flex;
    flex-direction: column;

    gap: 33px;

    @include ut.tablet {
      flex-direction: row;
      gap: 13px;
    }

    @include ut.desktop {
      gap: 21px;
    }
  }

  &__filter {
    display: flex;
    flex-direction: column;
    gap: 21px;

    background-color: #f5f5f5;

    max-width: 765px;
    padding: 24px 20px 31px 30px;

    @include ut.tablet {
      align-self: flex-start;
      gap: 20px;

      padding: 31px 47px 33px 30px;
    }

    @include ut.desktop {
      gap: 29px;

      padding: 31px 57px 49px 18px;
    }

    &-list {
      display: flex;
      flex-direction: column;

      gap: 10px;

      @include ut.tablet {
        gap: 12px;
      }

      @include ut.desktop {
        gap: 16px;
      }
    }

    &-title {
      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 19px;
      text-transform: uppercase;

      color: #2c2c2c;

      margin-left: 30px;

      @include ut.tablet {
        margin-left: 34px;
      }

      @include ut.desktop {
        margin-left: 38px;
      }
    }

    &-row {
      display: flex;
      align-items: center;

      gap: 10px;
    }
  }

  &__list {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    justify-content: center;

    @include ut.tablet {
      width: 100%;

      gap: 12px;

      margin-top: 27px;
    }

    @include ut.desktop {
      margin: 0;
      gap: 20px;
      justify-content: flex-start;
    }
  }

  &__item {
    display: flex;

    width: 100%;

    max-width: 350px;

    border: 2px solid #0020d0;
    border-radius: 10px;
    overflow: hidden;

    @include ut.tablet {
      flex-direction: column;
      max-width: 245px;

      border: 3px solid #0020d0;
      border-radius: 20px;
    }

    @include ut.desktop {
      max-width: 280px;
      max-height: 488px;

      height: 100%;

      justify-content: flex-start;
    }

    &_disable {
      .shop__item-price {
        color: #828282;
      }
      .shop__item-button {
        pointer-events: none;
        background: #bbbbbb;
      }
    }

    &-image {
      flex: 0 0 auto;
      width: 107px;

      overflow: hidden;

      @include ut.tablet {
        width: 100%;
      }

      &-source {
        width: 100%;
        height: 100%;

        &_mobile {
          display: flex;

          @include ut.tablet {
            display: none;
          }
        }

        &_tablet {
          display: none;

          @include ut.tablet {
            display: flex;
          }
          @include ut.desktop {
            display: none;
          }
        }

        &_desktop {
          display: none;

          @include ut.desktop {
            display: flex;
          }
        }
      }
    }

    &-info {
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      width: 100%;
      height: 100%;

      padding: 20px 13px 20px 11px;

      @include ut.tablet {
        padding: 34px 11px 31px 11px;
        gap: 16px;
      }

      @include ut.desktop {
        padding: 36px 17px 42px 16px;
      }

      &-wrapper {
        display: flex;
        flex-direction: column;

        gap: 9px;

        @include ut.tablet {
          gap: 11px;
        }

        @include ut.desktop {
          height: 149px;
          justify-content: space-between;
        }
      }
    }

    &-title {
      font-style: normal;
      font-weight: 500;
      font-size: 12px;
      line-height: 15px;
      text-transform: uppercase;

      color: #0020d0;

      @include ut.tablet {
        font-size: 15px;
        line-height: 19px;
      }

      @include ut.desktop {
        font-size: 16px;
        line-height: 19px;
      }
    }

    &-subtitle {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 17px;

      color: #2c2c2c;

      @include ut.tablet {
        font-size: 14px;
        line-height: 18px;
      }

      @include ut.desktop {
        font-size: 16px;
        line-height: 20px;
      }
    }

    &-price {
      font-style: normal;
      font-weight: 500;
      font-size: 12px;
      line-height: 15px;
      text-transform: uppercase;

      color: #0020d0;

      @include ut.tablet {
        font-size: 15px;
        line-height: 18px;

        margin-top: 5px;
      }
    }

    &-button {
      display: flex;
      align-items: center;
      justify-content: center;
      align-items: flex-end;

      width: 100%;

      outline: none;
      border: none;

      background: #0020d0;
      border-radius: 5px;

      padding: 6.5px 0;
      margin-top: 4px;

      @include ut.desktop {
        padding: 9px 0 10px 0%;
      }

      &-text {
        font-family: "Druk Wide Cyr";
        font-style: normal;
        font-weight: 500;
        font-size: 14px;
        line-height: 17px;
        text-align: center;
        text-transform: uppercase;

        color: #ffffff;

        @include ut.tablet {
          font-size: 15px;
          line-height: 18px;
        }

        @include ut.desktop {
          font-size: 16px;
          line-height: 19px;
        }
      }
    }
  }
}
</style>
