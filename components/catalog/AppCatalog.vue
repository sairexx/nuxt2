<template>
  <section class="catalog">
    <div class="catalog__container">
      <h2 class="catalog__title">каталог</h2>
      <div class="catalog__grid">
        <div class="catalog__item catalog__item_cow">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title"
              >Электропастухи для молочного и мясного КРС</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_shape">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title"
              >Электропастухи для овец и ягнят</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_horse">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title"
              >Электропастухи для лошадей и жеребят</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_goat">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title">Электропастухи для коз</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_pig">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title"
              >Электропастухи для свиней и поросят</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_rabbit">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title"
              >Электропастухи для птицы и мелких животных</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_bee">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title"
              >Электропастухи для защиты пасеки от медведя</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_universal">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title">Электропастухи универсальные</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
        <div class="catalog__item catalog__item_accessories">
          <div class="catalog__item-overlay"></div>
          <div class="catalog__item-info">
            <span class="catalog__item-title"
              >комплектующие для Электропастухов</span
            ><a class="catalog__item-link">Подробнее</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppCatalog",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.catalog {
  display: flex;
  justify-content: center;
  width: 100%;

  padding: 38px 39px 65px 39px;

  @include ut.tablet {
    padding-bottom: 50px;
  }

  @include ut.desktop {
    padding: 91px 39px 88px 39px;
  }

  &__container {
    display: flex;
    flex-direction: column;
    gap: 20px;

    width: 100%;
    max-width: 765px;

    @include ut.tablet {
      max-width: 765px;
      gap: 36px;
    }

    @include ut.desktop {
      max-width: 1180px;
      gap: 49px;
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
    flex-wrap: wrap;
    gap: 15px;

    @include ut.tablet {
      row-gap: 21px;
    }

    @include ut.desktop {
      column-gap: 20px;
      row-gap: 17px;
    }
  }

  &__item {
    position: relative;

    display: flex;
    align-items: flex-end;

    width: 100%;
    height: 222px;
    max-width: 350px;

    background-size: cover;
    background-repeat: no-repeat;

    @include ut.tablet {
      max-width: 375px;
    }

    @include ut.desktop {
      height: 359px;
      max-width: 380px;
    }

    &_cow {
      background-image: url("@/assets/images/cow-mobile-background.png");

      @include ut.tablet {
        background-image: url("@/assets/images/cow-tablet-background.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/cow-desktop-background.png");
      }
    }

    &_shape {
      background-image: url("@/assets/images/shape-mobile-background.png");

      @include ut.tablet {
        background-image: url("@/assets/images/shape-tablet-background.png");
      }

      @include ut.desktop {
        //background-image: url("@/assets/images/shape-desktop-background.png");
        background-image: url("@/assets/images/shape-tablet-background.png");
      }
    }

    &_horse {
      // margin-top: 2px;
      background-image: url("@/assets/images/horse-mobile-background.png");

      @include ut.tablet {
        background-image: url("@/assets/images/horse-tablet-background.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/horse-desktop-background.png");

        .catalog__item-title {
          font-size: 22px;
          line-height: 27px;
        }
      }
    }

    &_goat {
      background-image: url("@/assets/images/goat-mobile-background.png");

      @include ut.tablet {
        background-image: url("@/assets/images/goat-tablet-background.png");
      }

      @include ut.desktop {
        height: 391px;

        .catalog__item-overlay {
          height: 211px;
        }
        .catalog__item-title {
          font-size: 22px;
          line-height: 27px;
        }
        .catalog__item-info {
          height: 200px;
          gap: 79px;
          padding: 17px 29px;
        }

        .catalog__item-link {
          margin-left: -4px;
        }

        background-image: url("@/assets/images/goat-desktop-background.png");
      }
    }

    &_pig {
      margin-top: 2px;
      background-image: url("@/assets/images/pig-mobile-background.png");

      @include ut.tablet {
        margin-top: -1px;
        background-image: url("@/assets/images/pig-tablet-background.png");
      }

      @include ut.desktop {
        height: 391px;
        margin: 0;

        .catalog__item-overlay {
          height: 211px;
        }
        .catalog__item-title {
          font-size: 22px;
          line-height: 27px;
        }
        .catalog__item-info {
          height: 200px;
          padding: 17px 25px;
          gap: 80px;
        }

        background-image: url("@/assets/images/pig-desktop-background.png");
      }
    }

    &_rabbit {
      background-image: url("@/assets/images/rabbit-mobile-background.png");

      @include ut.tablet {
        margin-top: -1px;
        background-image: url("@/assets/images/rabbit-tablet-background.png");
      }

      @include ut.desktop {
        margin: 0;
        height: 391px;

        .catalog__item-overlay {
          height: 211px;
        }
        .catalog__item-title {
          font-size: 22px;
          line-height: 27px;
        }
        .catalog__item-info {
          height: 200px;
          padding: 17px 25px;
          gap: 80px;
        }

        background-image: url("@/assets/images/rabbit-desktop-background.png");
      }
    }

    &_bee {
      margin-top: 2px;
      background-image: url("@/assets/images/bee-mobile-background.png");

      @include ut.tablet {
        margin-top: -1px;
        background-image: url("@/assets/images/bee-tablet-background.png");
      }

      @include ut.desktop {
        margin: 0;
        height: 393px;
        margin-top: 2px;

        .catalog__item-overlay {
          height: 213px;
        }
        .catalog__item-title {
          font-size: 22px;
          line-height: 27px;
        }
        .catalog__item-info {
          height: 200px;
          padding: 15px 25px;
          gap: 80px;
        }

        background-image: url("@/assets/images/bee-desktop-background.png");
      }
    }

    &_universal {
      background-image: url("@/assets/images/universal-mobile-background.png");

      @include ut.tablet {
        background-image: url("@/assets/images/universal-tablet-background.png");
      }

      @include ut.desktop {
        height: 393px;
        margin-top: 2px;

        background-image: url("@/assets/images/universal-desktop-background.png");

        .catalog__item-overlay {
          height: 213px;
        }
        .catalog__item-title {
          font-size: 22px;
          line-height: 27px;
        }
        .catalog__item-info {
          height: 200px;
          padding: 15px 25px;
          gap: 80px;
        }
      }
    }

    &_accessories {
      background-image: url("@/assets/images/accessories-mobile-background.png");

      @include ut.tablet {
        background-image: url("@/assets/images/accessories-tablet-background.png");
      }

      @include ut.desktop {
        height: 393px;
        margin-top: 2px;

        .catalog__item-overlay {
          height: 213px;
        }
        .catalog__item-title {
          font-size: 20px;
          line-height: 24px;
        }
        .catalog__item-info {
          height: 200px;
          padding: 15px 25px;
          gap: 80px;
        }

        background-image: url("@/assets/images/accessories-desktop-background.png");
      }
    }

    &-image {
      position: absolute;
      top: 0;
      left: 0;

      width: 100%;
      height: 100%;
    }

    &-overlay {
      position: relative;

      width: 100%;
      height: 125px;

      margin-top: 97px;

      background: #0020d0;
      mix-blend-mode: multiply;
      z-index: 2;

      @include ut.desktop {
        height: 176px;
      }
    }

    &-info {
      position: absolute;
      bottom: 0;
      left: 0;

      width: 100%;
      height: 126px;

      display: flex;
      flex-direction: column;
      gap: 14px;

      padding: 15px 14px;
      z-index: 2;

      @include ut.tablet {
        gap: 16px;
        padding: 15px 17px;
      }

      @include ut.desktop {
        height: 164px;
        padding: 15px 25px;

        gap: 46px;
      }
    }

    &-title {
      height: 62px;
      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 21px;

      text-transform: uppercase;

      color: #ffffff;

      @include ut.desktop {
        font-size: 20px;
        line-height: 24px;
      }
    }

    &-link {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 17px;
      text-decoration-line: underline;

      color: #d9d9d9;

      @include ut.tablet {
        font-size: 15px;
        line-height: 18px;
      }

      @include ut.desktop {
        font-size: 16px;
        line-height: 20px;
      }
    }
  }
}
</style>
