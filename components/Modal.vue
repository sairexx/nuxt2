<script>
export default {
  name: "Modal",
  props: ["isVisible", "onHide"],
};
</script>

<template>
  <div class="modal">
    <div class="modal__header">
      <button @click="onHide">
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
    </div>
    <div class="modal__content">
      <slot></slot>
    </div>
  </div>
</template>

<style lang="scss"></style>
