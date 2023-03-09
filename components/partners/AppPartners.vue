<template>
  <section class="partners">
    <div class="partners__container">
      <h2 class="partners__title">нам доверяют</h2>
      <div class="partners__slider">
        <div class="partners__item partners__item_first">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-1.png"
            alt=""
          />
        </div>
        <div class="partners__item partners__item_second">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-2.png"
            alt=""
          />
        </div>
        <div class="partners__item partners__item_third">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-3.png"
            alt=""
          />
        </div>
        <div class="partners__item partners__item_fourth">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-4.png"
            alt=""
          />
        </div>
        <div class="partners__item partners__item_fifth">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-5.png"
            alt=""
          />
        </div>
        <div class="partners__item partners__item_sixth">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-6.png"
            alt=""
          />
        </div>
        <div class="partners__item partners__item_seventh">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-7.png"
            alt=""
          />
        </div>
        <div class="partners__item partners__item_eighth">
          <img
            class="partners__image"
            src="~/assets/images/about/partner-8.png"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppPartners",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.partners {
  display: flex;
  justify-content: center;
  width: 100%;

  &__container {
    display: flex;
    flex-direction: column;
    gap: 25px;

    width: 100%;
    max-width: 764px;

    padding: 54px 39px 20px 39px;

    @include ut.tablet {
      gap: 39px;
      padding: 80px 0 49px 0;
    }

    @include ut.desktop {
      max-width: 1180px;

      gap: 76px;

      padding: 89px 0 49px 0;
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
      line-height: 31px;
    }

    @include ut.desktop {
      font-size: 40px;
      line-height: 49px;
    }
  }

  &__slider {
    display: flex;
    align-items: center;
    flex-wrap: wrap;

    column-gap: 11px;
    row-gap: 14px;

    @include ut.tablet {
      gap: 12px;
    }

    @include ut.desktop {
      gap: 19px;
    }
  }

  &__item {
    &_first {
      width: 71px;
      height: 81px;

      @include ut.desktop {
        width: 110px;
        height: 126px;
      }
    }

    &_second {
      width: 82px;
      height: 81px;

      @include ut.desktop {
        width: 126px;
        height: 126px;
      }
    }

    &_third {
      width: 81px;
      height: 81px;

      @include ut.desktop {
        width: 126px;
        height: 126px;
      }
    }

    &_fourth {
      width: 81px;
      height: 81px;

      @include ut.desktop {
        width: 126px;
        height: 126px;
      }
    }

    &_fifth {
      width: 84px;
      height: 72px;

      @include ut.tablet {
        width: 96px;
        height: 82px;
      }

      @include ut.desktop {
        width: 147px;
        height: 126px;
      }
    }

    &_sixth {
      width: 65px;
      height: 72px;

      @include ut.tablet {
        width: 74px;
        height: 82px;
      }

      @include ut.desktop {
        width: 114px;
        height: 126px;
      }
    }

    &_seventh {
      width: 84px;
      height: 72px;

      @include ut.tablet {
        width: 96px;
        height: 82px;
      }

      @include ut.desktop {
        width: 147px;
        height: 126px;
      }
    }

    &_eighth {
      width: 84px;
      height: 46px;

      @include ut.tablet {
        width: 96px;
        height: 52px;
      }

      @include ut.desktop {
        width: 149px;
        height: 81px;
      }
    }
  }

  &__image {
    width: 100%;
    height: 100%;
  }
}
</style>
