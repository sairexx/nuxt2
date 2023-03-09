<script lang="ts">
import Logo from "./Logo.vue";
import NavBar from "./NavBar.vue";
import Button from "../Button.vue";
import Modal from "../Modal.vue";
import MenuIcon from "./MenuIcon.vue";
import BasketIcon from "./BasketIcon.vue";
import ModalForm from "./ModalForm.vue";

export default {
  name: "AppHeader",
  components: { NavBar, BasketIcon, MenuIcon, Logo, Modal, ModalForm },

  data() {
    const isVisibleModal = false;
    const isVisibleMenu = false;

    return {
      isVisibleMenu,
      isVisibleModal,
    };
  },
  methods: {
    setVisibleModal() {
      this.isVisibleModal = !this.isVisibleModal;
    },
  },
};
</script>

<template>
  <header class="header">
    <div class="header__container">
      <Logo />
      <NavBar />

      <div class="header__info">
        <div class="header__button">
          <Button title="Заказать звонок" :onClick="this.setVisibleModal" />
        </div>

        <BasketIcon />
        <MenuIcon />
        <Modal :isVisible="isVisibleModal" :onHide="this.setVisibleModal">
          <ModalForm></ModalForm>
        </Modal>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.header {
  display: flex;
  flex: 0 0 auto;
  align-items: center;
  justify-content: center;

  padding: 17px 52px 16px 39px;

  width: 100%;
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.15);

  @include ut.tablet {
    padding: 14px 0 14px 0;
  }

  @include ut.desktop {
    padding: 28px 0 29px 0;
  }

  &__container {
    display: flex;
    align-items: center;
    justify-content: space-between;

    width: 100%;

    @include ut.tablet {
      width: 764px;
    }

    @include ut.desktop {
      width: 1180px;
      justify-content: flex-start;
    }
  }

  &__logo {
    height: 27px;
    width: 110px;

    @include ut.tablet {
      width: 130px;
      height: 32px;
    }

    @include ut.desktop {
      height: 44px;
      width: 180px;
    }
  }

  &__info {
    display: flex;
    align-items: center;
    gap: 38px;
    margin: -6px -1px -2px 0px;

    @include ut.tablet {
      margin: 0 11px 0 0;
      gap: 36px;
    }

    @include ut.desktop {
      gap: 29px;

      margin-left: 39px;
    }
  }

  &__button {
    display: none;

    @include ut.desktop {
      display: flex;
      width: 247px;
    }
  }
}
</style>
