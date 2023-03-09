<script>
import Button from "../Button.vue";
export default {
  name: "ModalForm",
  components: { Button },
};
</script>

<template>
  <div class="container">
    <h2 class="container__title"></h2>
    <span class="container__description"></span>
    <input class="feedback__input" type="text" placeholder="Имя" />
    <input class="feedback__input" type="email" placeholder="E-mail" />
    <input class="feedback__input" type="number" placeholder="Номер телефона" />
    <Button />
  </div>
</template>

<style lang="scss" scoped></style>
