<template>
  <section class="guarantee">
    <div class="guarantee__wrapper">
      <div class="guarantee__container">
        <h2 class="guarantee__title">гарантия 18 месяцев</h2>
        <div class="guarantee__info">
          <span class="guarantee__text">
            Если с электропастухом СТАТИК-3М что-то случилось в разгар сезона,
            то мы всегда идем навстречу. По Вашему звонку отправляем новый
            прибор, а Вы отправляете нам неисправный.
          </span>
          <span class="guarantee__text">
            В этом случае электропастух возобновит свою работу максимально
            быстро. Не придется ждать, пока мы отремонтируем прибор и он
            вернется к Вам обратно.
          </span>
        </div>
        <span class="guarantee__notion">
          распространяется на неисправности, возникшие по причине заводского
          брака
        </span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppGuarantee",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.guarantee {
  display: flex;
  justify-content: center;

  width: 100%;

  padding: 29px 0 61px 0;

  @include ut.tablet {
    padding: 45px 0 47px 0;
  }

  @include ut.desktop {
    padding: 20px 0 25px 0;
  }

  &__wrapper {
    display: flex;
    align-items: center;
    flex-direction: column;

    width: 100%;
    max-width: 768px;
    height: 686px;
    padding: 0 40px 0 40px;

    background-position: center;
    background-repeat: no-repeat;
    background-image: url("~/assets/images/shipping/star.png");

    @include ut.tablet {
      align-items: flex-end;
      padding: 0;
      max-width: 100%;

      background-position: right;
      background-image: url("~/assets/images/shipping/guarantee-background-tablet.png");
    }

    @include ut.desktop {
      height: 911px;
      max-width: 1440px;

      padding: 50px 0;

      background-image: url("~/assets/images/shipping/guarantee-desktop-background.png");
    }
  }

  &__container {
    display: flex;
    flex-direction: column;
    gap: 16px;

    max-width: 383px;

    @include ut.tablet {
      gap: 19px;
      margin-right: 56px;
    }

    @include ut.desktop {
      max-width: 481px;
      margin-right: 129px;
    }
  }

  &__title {
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 22px;
    text-transform: uppercase;

    color: #ffffff;

    margin-top: 54%;

    @include ut.tablet {
      margin-top: 45%;
      font-size: 24px;
      line-height: 29px;
    }

    @include ut.desktop {
      margin-top: 35.6%;
      max-width: 366px;

      font-size: 40px;
      line-height: 49px;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;
    gap: 13px;

    @include ut.tablet {
      gap: 14px;
    }
  }

  &__text {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    color: #ffffff;

    @include ut.tablet {
      max-width: 310px;
    }

    @include ut.desktop {
      max-width: 479px;

      font-size: 18px;
      line-height: 24px;
    }
  }

  &__notion {
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;
    text-transform: uppercase;

    color: #ffffff;

    margin-top: 4px;

    @include ut.tablet {
      max-width: 310px;
      margin-top: 0;
    }

    @include ut.desktop {
      margin-top: 7px;
      max-width: 476px;

      font-size: 24px;
      line-height: 29px;
    }
  }
}
</style>
