<template>
  <section class="not-found">
    <div class="not-found__container">
      <div class="not-found__image">
        <img
          class="not-found__image-source"
          src="~/assets/images/404.png"
          alt=""
        />
      </div>
      <div class="not-found__info">
        <h2 class="not-found__title">что-то пошло не так...</h2>
        <span class="not-found__description"
          >Страница, на которую вы пытаетесь перейти, не найдена. Но вы можете
          вернуться <a class="not-found__link" href="">на главную.</a></span
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppNotFound",
};
</script>

<style lang="scss">
@use "@/assets/scss/styles/utils" as ut;
@use "@/assets/scss/styles/variables" as vars;

.not-found {
  display: flex;
  justify-content: center;

  width: 100%;

  padding: 89px 39px 91px 39px;

  @include ut.tablet {
    padding: 47px 0 91px 0;
  }

  @include ut.desktop {
    padding: 98px 0 0 0;
  }

  &__container {
    display: flex;
    align-items: center;
    flex-direction: column;

    width: 100%;

    gap: 27px;

    @include ut.tablet {
      align-items: center;
      flex-direction: row;

      max-width: 768px;
    }

    @include ut.desktop {
      max-width: 1183px;
    }
  }

  &__image {
    width: 350px;
    height: 367px;

    @include ut.tablet {
      flex: 0 0 auto;
      order: 2;

      width: 374px;
      height: 393px;
    }

    @include ut.desktop {
      width: 682px;
      height: 715px;
    }

    &-source {
      width: 100%;
      height: 100%;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;

    gap: 11px;

    @include ut.tablet {
      order: 1;

      gap: 20px;
      margin-top: -35px;
    }

    @include ut.desktop {
      margin-top: -80px;
      gap: 17px;
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
      line-height: 58px;
    }
  }

  &__description {
    font-family: vars.$montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;

    @include ut.tablet {
      font-size: 14px;
      line-height: 18px;
    }

    @include ut.desktop {
      font-size: 18px;
      line-height: 24px;
    }
  }

  &__link {
    color: #0020d0;
    text-decoration: underline;
  }
}
</style>
