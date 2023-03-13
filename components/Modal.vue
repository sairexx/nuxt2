<script>
export default {
  name: "Modal",
  props: {
    isVisible: {
      type: Boolean,
      required: true,
    },
    onHide: {
      type: Function,
      required: true,
    },
  },

  watch: {
    isVisible(newValue) {
      newValue
        ? document.body.classList.add("no-scroll")
        : document.body.classList.remove("no-scroll");
    },
  },
};
</script>

<template>
  <div v-if="isVisible" class="modal">
    <div class="modal__content">
      <button @click="onHide" class="modal__button">
        <svg
          width="23"
          height="24"
          viewBox="0 0 23 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
          class="modal__close"
        >
          <line
            x1="22.3613"
            y1="0.345611"
            x2="0.36132"
            y2="23.3456"
            stroke="#828282"
          />
          <line
            x1="0.361321"
            y1="0.654389"
            x2="22.3613"
            y2="23.6544"
            stroke="#828282"
          />
        </svg>
      </button>
      <slot />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.modal {
  position: absolute;
  top: 0;
  left: 0;

  width: 100%;
  height: 100%;

  padding: 0 19px;

  display: flex;
  justify-content: center;
  align-items: flex-start;

  overflow-y: auto;
  z-index: 999;
  background: rgba(44, 44, 44, 0.8);

  &__button {
    position: absolute;
    top: 11px;
    right: 6px;

    border: none;
    outline: none;
    background: transparent;

    @include ut.desktop {
      top: 17px;
      right: 12px;
    }
  }
  &__close {
    width: 15px;
    height: 15px;

    @include ut.tablet {
      width: 22px;
      height: 24px;
    }
  }

  &__content {
    display: flex;
    justify-content: center;

    position: relative;

    margin-top: 33px;
    padding: 25px 20px 33px 20px;

    width: 100%;
    max-width: 390px;
    z-index: 1000;

    background-color: white;

    @include ut.tablet {
      margin: 108px 0 0 0;
      max-width: 535px;
    }

    @include ut.desktop {
      margin: 251px 0 0 0;
      max-width: 820px;
    }
  }
}
</style>
