<template>
  <section class="reviews">
    <div class="reviews__container">
      <h2 class="reviews__title">отзывы</h2>
      <div class="reviews__grid">
        <div class="reviews__item reviews__item_cow">
          <span class="reviews__item-title"
            >Одуревшие быки под контролем, хозяин в восторге</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
        <div class="reviews__item reviews__item_neighbor">
          <span class="reviews__item-title"
            >сосед помогает ставить электропастух, искру проверяю на нем</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
        <div class="reviews__item reviews__item_interview">
          <span class="reviews__item-title"
            >Россия 24 — Интервью с российским производителем
            электропастухов</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
        <div class="reviews__item reviews__item_battle">
          <span class="reviews__item-title"
            >Наши против <br />
            французов — <br />
            Бородинская битва электропастухов</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
        <div class="reviews__item reviews__item_animals">
          <span class="reviews__item-title"
            >Животные рады, когда меня бьет током</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
        <div class="reviews__item reviews__item_cybershepherd">
          <span class="reviews__item-title"
            >электропастух от гималайского медведя. пасека хабаровска</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppReviews",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.reviews {
  display: flex;
  justify-content: center;

  width: 100%;

  padding: 38px 39px 60px 39px;

  @include ut.tablet {
    padding: 38px 0 65px 0;
  }

  @include ut.desktop {
    padding: 59px 0 100px 0;
  }

  &__container {
    display: flex;
    flex-direction: column;

    width: 100%;

    gap: 33px;

    @include ut.tablet {
      gap: 41px;
      max-width: 765px;
    }

    @include ut.desktop {
      gap: 81px;
      max-width: 1181px;
    }
  }

  &__title {
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 23px;

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
    gap: 10px;

    @include ut.tablet {
      column-gap: 15px;
      row-gap: 15px;
    }

    @include ut.desktop {
      column-gap: 20px;
      row-gap: 20px;
    }
  }

  &__item {
    position: relative;

    width: 100%;
    max-width: 350px;
    height: 205px;

    @include ut.tablet {
      max-width: 375px;
      height: 206px;
    }

    @include ut.desktop {
      max-width: 580px;
      height: 318px;
    }

    &_cow {
      background-image: url("@/assets/images/cow-mobile-review.png");

      @include ut.tablet {
        background-image: url("@/assets/images/cow-tablet-review.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/cow-desktop-review.png");
      }

      .reviews__item-title {
        width: 290px;
        margin: 0 0 6px 15px;

        @include ut.desktop {
          width: 326px;
          margin: 0 0 15px 18px;
        }
      }
    }

    &_neighbor {
      background-image: url("@/assets/images/neighbor-mobile-review.png");

      @include ut.tablet {
        background-image: url("@/assets/images/neighbor-tablet-review.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/neighbor-desktop-review.png");
      }

      .reviews__item-title {
        line-height: 19px;
        margin: 0 0 8px 15px;

        @include ut.desktop {
          font-size: 20px;
          line-height: 24px;

          width: 326px;

          margin: 0 0 15px 18px;
        }
      }

      .reviews__item-button {
        margin-top: 0;
        margin-left: 11px;
        width: 75px;

        @include ut.tablet {
          margin: 0;
        }
        @include ut.desktop {
          width: 108px;
        }
      }
    }

    &_interview {
      background-image: url("@/assets/images/interview-mobile-review.png");

      @include ut.tablet {
        background-image: url("@/assets/images/interview-mobile-review.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/interview-desktop-review.png");
      }

      .reviews__item-title {
        line-height: 19px;
        margin: 0 0 12px 14px;

        @include ut.tablet {
          margin: 0 0 9px 15px;
        }

        @include ut.desktop {
          font-size: 20px;
          line-height: 24px;

          margin: 0 0 18px 19px;
        }
      }
    }

    &_battle {
      background-image: url("@/assets/images/battle-mobile-review.png");

      @include ut.tablet {
        background-image: url("@/assets/images/battle-mobile-review.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/battle-desktop-review.png");
      }

      .reviews__item-title {
        margin: 0 0 14px 14px;
        width: 282px;
        line-height: 19px;

        @include ut.tablet {
          margin: 0 0 8px 15px;
        }

        @include ut.desktop {
          font-size: 20px;
          line-height: 24px;

          margin: 0 0 16px 18px;
          width: 360px;
        }
      }

      .reviews__item-button {
        margin-top: 0;
        margin-left: 11px;
        width: 75px;

        @include ut.tablet {
          margin: 0;
        }
        @include ut.desktop {
          width: 108px;
        }
      }
    }

    &_animals {
      background-image: url("@/assets/images/animals-mobile-preview.png");

      @include ut.tablet {
        background-image: url("@/assets/images/animals-mobile-preview.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/animals-desktop-preview.png");
      }

      .reviews__item-title {
        margin: 0 0 12px 14px;
        line-height: 19px;

        @include ut.tablet {
          margin: 0 0 7px 15px;
        }

        @include ut.desktop {
          font-size: 20px;
          line-height: 24px;

          margin: 0 0 17px 18px;
        }
      }
    }

    &_cybershepherd {
      background-image: url("@/assets/images/cybershepherd-mobile-review.png");

      @include ut.tablet {
        background-image: url("@/assets/images/cybershepherd-mobile-review.png");
      }

      @include ut.desktop {
        background-image: url("@/assets/images/cybershepherd-desktop-review.png");
      }

      .reviews__item-title {
        margin: 0 0 14px 14px;
        line-height: 19px;

        @include ut.tablet {
          margin: 0 0 8px 16px;
        }

        @include ut.desktop {
          font-size: 20px;
          line-height: 24px;

          margin: 0 0 17px 18px;

          width: 305px;
        }
      }
    }

    &-image {
      position: absolute;
      top: 0;
      left: 0;

      width: 100%;
      height: 100%;
    }

    &-title {
      position: absolute;
      bottom: 0;
      left: 0;

      z-index: 2;

      margin: 0 0 10px 14px;

      width: 265px;

      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 21px;

      text-transform: uppercase;

      color: #ffffff;

      @include ut.tablet {
        font-size: 16px;
        line-height: 19px;
        width: 295px;
      }

      @include ut.desktop {
        font-size: 20px;
        line-height: 24px;
      }
    }

    &-button {
      position: absolute;
      top: 50%;
      left: 50%;

      transform: translateY(-50%) translateX(-50%);

      display: flex;
      align-items: center;
      justify-content: center;

      margin-top: -6px;

      width: 71px;

      outline: none;
      border: none;
      background: none;

      z-index: 3;

      @include ut.tablet {
        width: 74px;
        margin: 0;
      }

      @include ut.desktop {
        width: 108px;
      }

      &-image {
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>
