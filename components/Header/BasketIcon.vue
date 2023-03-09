<template>
  <div class="basket">
    <img class="basket__icon" src="@/assets/icons/shopping-cart.svg" alt="" />
    <div class="basket__badge">
      <svg
        width="15"
        height="16"
        class="basket__star"
        viewBox="0 0 15 16"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M7.5 0.277588L9.3541 2.07125L11.9084 1.70996L12.3541 4.25088L14.6329 5.45996L13.5 7.77759L14.6329 10.0952L12.3541 11.3043L11.9084 13.8452L9.3541 13.4839L7.5 15.2776L5.6459 13.4839L3.09161 13.8452L2.6459 11.3043L0.367076 10.0952L1.5 7.77759L0.367076 5.45996L2.6459 4.25088L3.09161 1.70996L5.6459 2.07125L7.5 0.277588Z"
          fill="#828282"
        />
      </svg>
      <span class="basket__count">1</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "BasketIcon",
};
</script>

<style lang="scss" scoped>
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;
.basket {
  position: relative;

  margin: -3px 2px 0 0;

  &__icon {
    width: 25px;
    height: 21px;

    @include ut.tablet {
      width: 32px;
      height: 32px;
    }

    @include ut.desktop {
      width: 39px;
      height: 35px;
    }
  }

  &__badge {
    position: absolute;
    top: 0;
    right: 0;

    display: flex;
    justify-content: center;
    align-items: center;

    margin: 4px -3px 0 0;
    z-index: 2;
  }

  &__star {
  }

  &__count {
    position: absolute;
    top: 50%;

    transform: translateX(-50%);
    transform: translateY(-50%);

    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 700;
    font-size: 10px;
    line-height: 12px;
    text-align: center;
    text-transform: uppercase;

    color: #ffffff;
  }
}
</style>
