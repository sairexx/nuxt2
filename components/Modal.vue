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

  display: flex;
  align-items: center;
  justify-content: center;

  width: 100%;
  height: 100%;

  background: rgba(44, 44, 44, 0.8);
  z-index: 999;

  /* &__header {
    display: flex;
    align-items: center;
    justify-content: flex-end;

    width: 100%;
    max-width: 390px;

    padding: 18px 20px 0 20px;

    @include ut.tablet {
      max-width: ;
    }

    @include ut.desktop {
    }
  } */

  &__button {
    position: absolute;
    top: 0;
    right: 0;
  }
  &__close {
  }

  &__content {
    position: relative;
    background-color: white;
  }
}
</style>
