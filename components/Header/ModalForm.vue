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
    <form action="">
      <input class="container__input" type="text" placeholder="Имя" />
      <input class="container__input" type="email" placeholder="E-mail" />
      <input
        class="container__input"
        type="number"
        placeholder="Номер телефона"
      />
      <Button title="Заказать звонок" type="submit" :on-click="acceptCall" />
    </form>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;
.container {
  display: flex;
  flex-direction: column;

  &__title {
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
      font-size: 40px;
      line-height: 51px;
    }
  }

  &__description {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    @include ut.tablet {
    }

    @include ut.desktop {
    }
  }

  &__input {
  }
}
</style>
