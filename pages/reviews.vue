<template>
  <div>
    <AppReviews />
    <AppFeedbackForm />
  </div>
</template>

<script>
import AppReviews from "~/components/reviews/AppReviews.vue";
import AppFeedbackForm from "~/components/FeedbackForm/AppFeedbackForm.vue";

export default {
  name: "Reviews",
  components: {
    AppReviews,
    AppFeedbackForm,
  },
};
</script>

<style lang="scss"></style>
