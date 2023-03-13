<script>
export default {
  name: "Button",
  props: {
    title: {
      type: String,
      required: true,
    },
    isWide: {
      type: Boolean,
      required: false,
    },
    onClick: {
      type: Function,
      required: true,
    },
  },
};
</script>

<template>
  <button :class="[{ ['button_wide']: isWide }, 'button']" @click="onClick">
    <span class="button__title">{{ title }}</span>
  </button>
</template>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.button {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 100%;

  padding: 17px 20px 15px 20px;

  background-color: transparent;
  border: 2px solid #0020d0;
  border-radius: 5px;

  transition: border-color vars.$transition-duration ease-in-out;

  &:hover {
    border-color: #1657ff;

    transition: border-color vars.$transition-duration ease-in-out;

    .button__title {
      color: #1657ff;

      transition: color vars.$transition-duration ease-in-out;
    }
  }

  &:active {
    border-color: #5887ff;

    .button__title {
      color: #5887ff;
    }
  }

  &_wide {
    padding: 9px 43px 9px 20px;

    .button__title {
      @include ut.tablet {
        font-size: 18px;
        line-height: 22px;
      }

      @include ut.desktop {
        font-size: 24px;
        line-height: 29px;
      }
    }

    @include ut.tablet {
      padding: 16px 20px 18px 20px;
    }

    @include ut.desktop {
      padding: 29px 20px 20px 20px;
    }
  }

  &__title {
    font-family: vars.$druk-cyr;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 17px;
    text-align: center;
    text-transform: uppercase;

    color: #0020d0;
    transition: color vars.$transition-duration ease-in-out;
  }
}
</style>
