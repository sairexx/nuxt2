<template>
  <section class="videos">
    <div class="videos__container">
      <div class="videos__header">
        <h2 class="videos__title">отзывы</h2>
        <a class="videos__link" href="">Смотреть все отзывы</a>
      </div>
      <div class="videos__list">
        <div class="reviews__item reviews__item_cow">
          <span class="reviews__item-title"
            >Одуревшие быки под контролем, хозяин в восторге</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
        <div class="reviews__item reviews__item_neighbor">
          <span class="reviews__item-title"
            >сосед помогает ставить электропастух, искру проверяю на нем</span
          >
          <button class="reviews__item-button">
            <img
              class="reviews__item-button-image"
              src="~/assets/icons/youtube.svg"
              alt=""
            />
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppVideos",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.videos {
  display: flex;
  justify-content: center;

  width: 100%;

  &__container {
    display: flex;
    flex-direction: column;
    gap: 33px;

    width: 100%;
    max-width: 765px;

    padding: 36px 39px 60px 39px;

    @include ut.tablet {
      gap: 40px;

      padding: 41px 0 90px 0;
    }

    @include ut.desktop {
      padding: 91px 0 102px 0;
      gap: 29px;

      max-width: 1178px;
    }
  }

  &__header {
    display: flex;
    align-items: flex-end;
    gap: 23px;

    @include ut.tablet {
      gap: 34px;
    }

    @include ut.desktop {
      gap: 37px;
    }
  }

  &__title {
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 23px;

    text-transform: uppercase;
    color: #0020d0;

    @include ut.tablet {
      font-size: 24px;
      line-height: 31px;
    }

    @include ut.desktop {
      font-size: 40px;
      line-height: 49px;
    }
  }

  &__link {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 15px;
    line-height: 18px;
    text-decoration-line: underline;
    color: #2c2c2c;

    @include ut.desktop {
      margin: 0 0 3px 0;

      font-size: 20px;
      line-height: 24px;
    }
  }

  &__list {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;

    @include ut.tablet {
      flex-wrap: nowrap;
    }

    @include ut.desktop {
      gap: 22px;
    }
  }
}
</style>
