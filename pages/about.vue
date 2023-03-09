<template>
  <div>
    <AppAbout />
    <AppDocument />
    <AppExhibitions />
    <AppAdvantages />
    <AppPartners />
    <AppVideos />
    <AppFeedbackForm />
  </div>
</template>

<script>
import AppVideos from "~/components/videos/AppVideos.vue";
import AppAbout from "~/components/about/about/AppAbout.vue";
import AppAdvantages from "~/components/advantages/AppAdvantages.vue";
import AppPartners from "~/components/partners/AppPartners.vue";
import AppDocument from "~/components/about/documents/AppDocument.vue";
import AppFeedbackForm from "~/components/FeedbackForm/AppFeedbackForm.vue";
import AppExhibitions from "~/components/about/exhibitions/AppExhibitions.vue";

export default {
  name: "About",
  components: {
    AppAbout,
    AppVideos,
    AppDocument,
    AppPartners,
    AppAdvantages,
    AppExhibitions,
    AppFeedbackForm,
  },
};
</script>

<style lang="scss"></style>
