<template>
  <section class="feedback">
    <div class="feedback__container">
      <div class="feedback__logo"></div>
      <div class="feedback__form">
        <div class="feedback__info">
          <h2 class="feedback__title">остались вопросы?</h2>
          <span class="feedback__subtitle"
            >Укажите ваш номер телефона, и мы свяжемся с вами в течение двух
            минут</span
          >
        </div>
        <div class="feedback__fields">
          <input class="feedback__input" type="text" placeholder="Имя" />
          <input class="feedback__input" type="email" placeholder="E-mail" />
          <input
            class="feedback__input"
            type="number"
            placeholder="Номер телефона"
          />
          <button class="feedback__button">
            <span class="feedback__button-text">связаться с нами</span>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppFeedbackForm",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.feedback {
  display: flex;
  align-items: center;
  flex-direction: column;

  padding: 42px 38px 45px 40px;

  width: 100%;
  background: #0020d0;

  @include ut.tablet {
    padding: 42px 38px 69px 0;
  }

  &__container {
    display: flex;
    align-items: center;
    flex-direction: column;
    gap: 23px;

    width: 100%;
    max-width: 1440px;

    @include ut.tablet {
      gap: 80px;
      flex-direction: row;
    }

    @include ut.desktop {
      gap: 79px;
    }
  }

  &__logo {
    width: 200px;
    height: 200px;

    background-position: center;
    background-repeat: no-repeat;
    background-image: url("@/assets/images/feedback-mobile-logo.png");

    @include ut.tablet {
      height: 571px;
      width: 506px;

      background-size: 375px;
      background-position-x: 0px;
      background-position-y: 34px;

      background-image: url("@/assets/images/feedback-tablet-background.png");
    }

    @include ut.desktop {
      flex: 0 0 auto;

      height: 790px;
      width: 551px;

      background-size: 520px;
      background-position-x: 1px;
      background-position-y: 38px;
    }
  }

  &__form {
    display: flex;
    flex-direction: column;
    gap: 29px;

    @include ut.tablet {
      gap: 29px;
      align-self: flex-start;
      margin-top: 70px;
    }

    @include ut.desktop {
      margin-top: 133px;
      gap: 55px;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;
    gap: 13px;

    @include ut.desktop {
      gap: 17px;
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
      width: 200px;
      font-size: 24px;
      line-height: 31px;
    }

    @include ut.desktop {
      font-size: 40px;
      line-height: 49px;
      width: 100%;
    }
  }

  &__subtitle {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    color: #ffffff;

    @include ut.tablet {
      width: 82%;
      font-size: 18px;
      line-height: 23px;
    }

    @include ut.desktop {
      font-size: 24px;
      line-height: 29px;
      width: 500px;
    }
  }

  &__fields {
    display: flex;
    flex-direction: column;
    gap: 15px;

    @include ut.desktop {
      gap: 19px;
    }
  }

  &__input {
    padding: 13px 0 9px 16px;
    background: rgba(238, 238, 238, 0.5);
    border-radius: 5px;
    border: none;

    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;
    color: #f5f5f5;

    &::placeholder {
      font-family: vars.$montserrat;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;
      color: #f5f5f5;

      @include ut.tablet {
        font-size: 18px;
        line-height: 23px;
      }

      @include ut.desktop {
        font-size: 24px;
        line-height: 29px;
      }
    }

    @include ut.tablet {
      padding: 17.88px 0 19px 17px;

      font-size: 18px;
      line-height: 23px;

      max-width: 376px;
    }

    @include ut.desktop {
      padding: 25px 0 24px 20px;

      font-size: 24px;
      line-height: 29px;
      max-width: unset;
    }
  }

  &__button {
    display: flex;
    align-items: center;
    justify-content: center;

    outline: none;
    background-color: transparent;

    border: 3px solid #ffffff;
    border-radius: 8px;

    padding: 10px 0 7px 0;

    @include ut.tablet {
      max-width: 376px;

      padding: 17px 0 15px 0;
    }

    @include ut.desktop {
      max-width: unset;
      padding: 25px 0 22px 0;
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
        font-size: 18px;
        line-height: 22px;
      }

      @include ut.desktop {
        font-size: 24px;
        line-height: 29px;
      }
    }
  }
}
</style>
