<script>
import Button from "../Button.vue";

export default {
  name: "ModalForm",
  components: { Button },
  methods: {
    acceptCall() {
      console.log("вы заказали звонок");
    },
  },
};
</script>

<template>
  <div class="container">
    <h2 class="container__title">Заказать звонок</h2>
    <span class="container__description">
      Укажите ваш номер телефона, и мы свяжемся с вами в течение двух минут
    </span>
    <form action="" class="container__fields">
      <input class="container__input" type="text" placeholder="Имя" />
      <span class="container__error container__error_hidden"
        >ошибка валидации</span
      >
      <input class="container__input" type="email" placeholder="E-mail" />
      <input
        class="container__input"
        type="number"
        placeholder="Номер телефона"
      />
      <Button
        type="submit"
        title="Заказать звонок"
        :is-wide="true"
        :on-click="acceptCall"
      />
    </form>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;
.container {
  display: flex;
  flex-direction: column;

  width: 100%;

  max-width: 375px;

  padding: 15px 0 0 0;

  @include ut.tablet {
    padding: 19px 0 20px 0;
  }

  @include ut.desktop {
    max-width: 580px;
    padding: 45px 0 56px 0;
  }

  .button {
    @include ut.desktop {
      margin-top: 5px;
    }
  }

  &__title {
    font-family: vars.$druk-wide;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 23px;

    text-align: center;
    text-transform: uppercase;

    color: #0020d0;

    @include ut.tablet {
      font-weight: 700;
      font-size: 24px;
      line-height: 31px;
    }

    @include ut.desktop {
      font-family: vars.$default-font;
      font-size: 40px;
      line-height: 51px;
    }
  }

  &__description {
    margin-top: 31px;

    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    @include ut.tablet {
      margin-top: 22px;

      font-size: 18px;
      line-height: 23px;
    }

    @include ut.desktop {
      margin-top: 33px;

      font-size: 24px;
      line-height: 29px;
    }
  }

  &__fields {
    display: flex;
    flex-direction: column;

    gap: 15px;

    margin-top: 32px;

    @include ut.tablet {
      margin-top: 20px;
    }

    @include ut.desktop {
      margin-top: 54px;

      gap: 16px;
    }
  }

  &__error {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    color: red;

    @include ut.tablet {
      font-size: 18px;
      line-height: 23px;
    }

    @include ut.desktop {
      font-size: 24px;
      line-height: 29px;
    }

    &_visible {
      display: flex;
    }

    &_hidden {
      display: none;
    }
  }
  &__input {
    padding: 11px 11px 9px 11px;
    border-radius: 5px;
    background: #f5f5f5;
    border: 1px solid #bbbbbb;

    font-family: "Montserrat";
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    &_invalid {
      border-color: red;
    }

    &::placeholder {
      color: #828282;
    }

    @include ut.tablet {
      font-size: 18px;
      line-height: 23px;
      padding: 19px 11px 16px 11px;
    }

    @include ut.desktop {
      font-size: 24px;
      line-height: 29px;
      padding: 25px 15px 24px 15px;
    }
  }
}
</style>
