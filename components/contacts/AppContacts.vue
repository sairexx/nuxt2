<script>
export default {
  name: "AppContacts",
};
</script>

<template>
  <section class="contacts">
    <div class="contacts__container">
      <h2 class="contacts__title">контакты</h2>
    </div>
    <div class="contacts__content">
      <div class="contacts__info">
        <h3 class="contacts__info-title">
          ООО «НПК «Стамакс» <br />
          Завод-изготовитель электропастухов «Статик-3М» и комплектующих к ним
        </h3>
        <address class="contacts__info-address">
          Россия, Алтайский край, г. Барнаул, проспект Космонавтов, 6/1
          (ориентир — АЗС «Роснефть»)
        </address>
        <div class="contacts__info-communications">
          <span class="contacts__info-number">8-800-550-04-85</span
          ><span class="contacts__info-mail">sale@staremax.com</span>
        </div>
      </div>

      <div ref="map" class="contacts__map">
        <iframe
          src="https://yandex.ru/map-widget/v1/?um=constructor%3A8417eea5799572fdc2a4bed24d44ac34e794f9283cc9fab230a82b946449129d&amp;source=constructor"
          width="100%"
          height="720"
          frameborder="0"
          class="contacts__map-source contacts__map-source_desktop"
        ></iframe>
        <iframe
          src="https://yandex.ru/map-widget/v1/?um=constructor%3A8417eea5799572fdc2a4bed24d44ac34e794f9283cc9fab230a82b946449129d&amp;source=constructor"
          width="100%"
          height="500"
          frameborder="0"
          class="contacts__map-source contacts__map-source_tablet"
        ></iframe>
        <iframe
          src="https://yandex.ru/map-widget/v1/?um=constructor%3A8417eea5799572fdc2a4bed24d44ac34e794f9283cc9fab230a82b946449129d&amp;source=constructor"
          width="100%"
          height="240"
          frameborder="0"
          class="contacts__map-source contacts__map-source_mobile"
        ></iframe>
      </div>
    </div>

    <div class="contacts__container">
      <div class="contacts__details">
        <h2 class="contacts__details-title">банковские реквизиты</h2>
        <div class="contacts__details-list">
          <div class="contacts__details-row">
            <span class="contacts__details-key">Организация </span
            ><span class="contacts__details-value">ООО «НПК «Стамакс»</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">ИНН</span
            ><span class="contacts__details-value">2225136205</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">КПП</span
            ><span class="contacts__details-value">226301001</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">Счёт</span
            ><span class="contacts__details-value">40702810304000013220</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">Банк </span
            ><span class="contacts__details-value"
              >Сибирский филиал ПАО "Промсвязьбанк" в г. Новосибирск</span
            >
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">К/С</span
            ><span class="contacts__details-value">30101810500000000816</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">БИК </span
            ><span class="contacts__details-value">045004816</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">ОГРН</span
            ><span class="contacts__details-value">1132225001611</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">ОКПО</span
            ><span class="contacts__details-value">10050625</span>
          </div>
          <div class="contacts__details-row">
            <span class="contacts__details-key">ОКВЭД</span
            ><span class="contacts__details-value">73.10</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.contacts {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;

  width: 100%;
  padding: 38px 0 48px 0;

  gap: 30px;

  @include ut.tablet {
    gap: 56px;

    padding: 38px 0 64px 0;
  }

  @include ut.desktop {
    padding: 57px 0 81px 0;

    gap: 31px;
  }

  &__container {
    display: flex;
    flex-direction: column;
    padding: 0 39px;
    gap: 30px;

    width: 100%;

    @include ut.tablet {
      padding: 0;

      max-width: 764px;
    }

    @include ut.desktop {
      max-width: 1180px;
    }
  }

  &__map-source {
    &_desktop {
      display: none;

      @include ut.desktop {
        display: flex;
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

    &_mobile {
      display: flex;

      @include ut.tablet {
        display: none;
      }
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
      line-height: 58px;
    }
  }

  &__content {
    position: relative;

    display: flex;
    flex-direction: column;
    gap: 32px;

    width: 100%;

    @include ut.tablet {
      height: 500px;
    }

    @include ut.desktop {
      height: 760px;
      max-width: 1440px;
    }
  }

  &__map {
    width: 100%;

    @include ut.tablet {
      position: absolute;
      top: 0;
      left: 0;

      width: 100%;
      height: 100%;
    }
  }

  &__image {
    width: 100%;

    @include ut.tablet {
      height: 100%;
    }

    &_mobile {
      @include ut.tablet {
        display: none;
      }
    }

    &_tablet {
      display: none;

      @include ut.tablet {
        display: flex;
        object-fit: cover;
      }
    }
  }

  &__info {
    display: flex;
    flex-direction: column;
    gap: 19.5px;

    padding: 0 39px;

    @include ut.tablet {
      position: absolute;
      top: 76px;
      left: 130px;

      width: 100%;

      padding: 52px 19px 59px 17px;

      z-index: 2;
      background-color: white;

      max-width: 505px;

      gap: 22px;
    }

    @include ut.desktop {
      top: 93px;
      padding: 71px 24px 87px 21px;
      max-width: 680px;

      gap: 40px;
    }

    &-title {
      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 21px;

      text-transform: uppercase;

      color: #2c2c2c;

      width: 305px;

      @include ut.tablet {
        width: 420px;
      }

      @include ut.desktop {
        font-size: 24px;
        line-height: 29px;

        width: 591px;
      }
    }

    &-address {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 15px;
      line-height: 19px;

      color: #2c2c2c;

      width: 288px;

      @include ut.tablet {
        font-size: 18px;
        line-height: 23px;

        width: 350px;
      }

      @include ut.desktop {
        font-size: 24px;
        line-height: 29px;

        width: 469px;
      }
    }

    &-communications {
      display: flex;
      flex-direction: column;

      @include ut.tablet {
        margin-top: -7px;
      }
    }

    &-number,
    &-mail {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 15px;
      line-height: 19px;

      color: #2c2c2c;

      @include ut.tablet {
        font-size: 18px;
        line-height: 23px;
      }

      @include ut.desktop {
        font-size: 22px;
        line-height: 27px;
      }
    }
  }

  &__details {
    display: flex;
    flex-direction: column;
    margin-top: 17px;
    gap: 27px;

    @include ut.tablet {
      gap: 37px;

      margin-top: 15px;
    }

    @include ut.desktop {
      margin-top: 72px;
      gap: 45px;
    }

    &-title {
      font-style: normal;
      font-weight: 500;
      font-size: 22px;
      line-height: 27px;
      text-transform: uppercase;

      color: #0020d0;
    }

    &-list {
      display: flex;
      flex-direction: column;
    }

    &-row {
      display: flex;
      gap: 18px;

      @include ut.tablet {
        gap: 79px;
      }

      @include ut.desktop {
        gap: 74px;
      }
    }

    &-key {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 700;
      font-size: 14px;
      line-height: 18px;

      color: #2c2c2c;

      min-width: 102px;

      @include ut.tablet {
        font-size: 16px;
        line-height: 24px;

        min-width: 116px;
      }

      @include ut.desktop {
        font-size: 18px;
        line-height: 24px;

        min-width: 130px;
      }
    }

    &-value {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #2c2c2c;

      @include ut.tablet {
        font-size: 16px;
        line-height: 24px;
      }

      @include ut.desktop {
        font-size: 18px;
        line-height: 24px;
      }
    }
  }
}
</style>
