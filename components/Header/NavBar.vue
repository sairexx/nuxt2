<template>
  <nav class="navigation">
    <ul class="navigation__list">
      <li class="navigation__item">
        <NuxtLink class="navigation__link" to="/catalog">Каталог</NuxtLink>
      </li>

      <li class="navigation__item">
        <NuxtLink class="navigation__link" to="/shipping">как купить</NuxtLink>
      </li>

      <li class="navigation__item">
        <NuxtLink class="navigation__link" to="/about">о компании</NuxtLink>
      </li>

      <li class="navigation__item">
        <NuxtLink class="navigation__link" to="/contacts">Контакты</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.navigation {
  display: none;

  @include ut.desktop {
    display: flex;
    margin-left: 44px;
  }

  &__list {
    display: flex;
    align-items: center;
  }

  &__item {
    a {
      outline: none;
    }

    &:nth-child(2) {
      margin-left: 31px;
    }

    &:nth-child(3) {
      margin-left: 37px;
    }

    &:nth-child(4) {
      margin-left: 39px;
    }
  }

  &__link {
    font-size: 14px;
    font-weight: 500;
    line-height: 17px;
    font-style: normal;
    text-transform: uppercase;

    outline: none;

    color: #2c2c2c;
    white-space: nowrap;
  }
}
</style>
