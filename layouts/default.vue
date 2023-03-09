<template>
  <section class="root-container">
    <AppHeader />
    <AppContent>
      <Nuxt />
    </AppContent>
    <AppFooter />
  </section>
</template>

<script>
import AppHeader from "~/components/Header/AppHeader.vue";
import AppContent from "~/components/AppContent.vue";
import AppFooter from "~/components/AppFooter.vue";
export default {
  name: "default",
  components: {
    AppFooter,
    AppContent,
    AppHeader,
  },

  async asyncData({ $dataApi }) {
    return {
      menu: (await $dataApi.getMenu()).json,
    };
  },
};
</script>

<style></style>
