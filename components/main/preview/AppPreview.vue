<template>
  <section class="preview">
    <div class="preview__container">
      <div class="preview__frame">
        <img
          class="preview__frame-source preview__frame-source_tablet"
          src="~/assets/images/main/preview-frame-tablet.png"
          alt=""
        /><img
          class="preview__frame-source preview__frame-source_desktop"
          src="~/assets/images/main/preview-frame-desktop.png"
          alt=""
        />
      </div>
      <div class="preview__star"></div>
      <div class="preview__wrapper">
        <h2 class="preview__title">электропастух «Статик-3М»</h2>
        <span class="preview__text"
          >Мы — завод-изготовитель электропастухов «Статик-3М» и комплектующих к
          ним. С 2013 года производим и продаем электропастухи. Гарантируем
          лучшие цены и быстрое сервисное обслуживание</span
        ><span class="preview__text preview__text_tablet"
          >Мы — завод-изготовитель <br />
          электропастухов «Статик-3М» и <br />
          комплектующих к ним. С 2013 года <br />
          производим и продаем <br />
          электропастухи. Гарантируем лучшие <br />
          цены и быстрое сервисное <br />
          обслуживание</span
        ><span class="preview__text preview__text_desktop"
          >Мы — завод-изготовитель <br />
          электропастухов «Статик-3М» и <br />
          комплектующих к ним. С 2013 года <br />
          производим и продаем <br />
          электропастухи. Гарантируем <br />
          лучшие цены и быстрое сервисное <br />
          обслуживание</span
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppPreview",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.preview {
  position: relative;

  display: flex;
  justify-content: center;

  width: 100%;

  &__container {
    position: relative;

    display: flex;
    justify-content: flex-start;
    align-items: flex-end;
    width: 100%;
    height: 864px;

    background-size: cover;
    background-repeat: no-repeat;
    background-image: url("~/assets/images/main/preview-background-mobile.png");

    @include ut.tablet {
      height: 621px;
      max-width: 1024px;

      background-position-y: -60px;
      background-image: url("~/assets/images/main/preview-background-tablet.png");
    }

    @include ut.desktop {
      max-width: 1440px;
      height: 914px;

      backdrop-filter: 20px;
      background-position-y: -110px;
      background-image: url("~/assets/images/main/preview-background-desktop.png");
    }
  }

  &__frame {
    display: none;

    position: absolute;
    top: 0;
    left: 0;

    width: 100%;
    height: 100%;

    align-items: center;
    justify-content: center;
    z-index: 2;

    @include ut.tablet {
      display: flex;
    }

    &-source {
      &_tablet {
        display: flex;

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

  &__star {
    position: absolute;
    bottom: 0;
    left: 0;

    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    gap: 9px;

    padding: 0 39px 32px 39px;

    width: 100%;
    height: 431.59px;

    max-width: 638.19px;
    background-repeat: no-repeat;
    background-position: center;
    background-image: url("~/assets//images/main/wrapper-mobile.png");
    mix-blend-mode: multiply;

    @include ut.tablet {
      max-width: unset;
      width: 720.2px;
      height: 482.98px;

      gap: 9px;
      padding: 0 39px 101px 196px;
      background-image: url("~/assets//images/main/wrapper-tablet.png");
    }

    @include ut.desktop {
      padding: 0 48px 129px 229px;
      gap: 23px;
      width: 1037px;
      height: 699.81px;

      background-image: url("~/assets//images/main/wrapper-desktop.png");
    }
  }

  &__wrapper {
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    gap: 9px;

    padding: 0 39px 32px 39px;

    width: 100%;
    height: 431.59px;

    max-width: 638.19px;

    z-index: 2;

    @include ut.tablet {
      max-width: unset;
      width: 720.2px;
      height: 482.98px;

      gap: 9px;
      padding: 0 39px 101px 196px;
    }

    @include ut.desktop {
      width: 1037px;
      height: 699.81px;

      padding: 0 48px 129px 229px;

      gap: 23px;
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
      line-height: 49px;
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
      display: none;
      max-width: 380px;

      font-size: 16px;
      line-height: 20px;
    }

    @include ut.desktop {
      max-width: 580px;

      font-size: 24px;
      line-height: 29px;
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
</style>
