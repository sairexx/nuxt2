<template>
  <div>
    <AppPreview />
    <AppInfo />
    <AppGenerator />
    <div class="main__catalog">
      <AppCatalog />
    </div>
    <AppAdvantages />
    <AppPartners />
    <AppVideos />
    <AppFeedbackForm />
  </div>
</template>

<script>
import AppPreview from "~/components/main/preview/AppPreview.vue";
import AppInfo from "~/components/main/info/AppInfo.vue";
import AppGenerator from "~/components/main/generator/AppGenerator.vue";
import AppCatalog from "~/components/catalog/AppCatalog.vue";
import AppAdvantages from "~/components/advantages/AppAdvantages.vue";
import AppVideos from "~/components/videos/AppVideos.vue";
import AppFeedbackForm from "~/components/FeedbackForm/AppFeedbackForm.vue";
import AppPartners from "~/components/partners/AppPartners.vue";

export default {
  name: "Main",
  components: {
    AppPartners,
    AppPreview,
    AppInfo,
    AppGenerator,
    AppCatalog,
    AppAdvantages,
    AppVideos,
    AppFeedbackForm,
  },
};
</script>

<style lang="scss"></style>
