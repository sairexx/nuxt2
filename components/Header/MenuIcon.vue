<template>
  <div class="menu">
    <div class="menu__vector"></div>
    <div class="menu__vector"></div>
    <div class="menu__vector"></div>
  </div>
</template>

<script>
export default {
  name: "MenuIcon",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.menu {
  display: flex;
  flex-direction: column;
  gap: 6px;

  width: 23px;

  margin: 3px 1px 0px 0px;

  @include ut.tablet {
    width: 26px;
    margin-bottom: 5px;
  }

  @include ut.desktop {
    display: none;
  }

  &__vector {
    width: 100%;
    height: 2px;

    background-color: #828282;
  }
}
</style>
