<template>
  <div>
    <AppConditions />
    <AppGuide />
    <AppDelivery />
    <AppPickup />
    <AppGuarantee />
    <AppFeedbackForm />
  </div>
</template>

<script>
import AppGuide from "~/components/shipping/guide/AppGuide.vue";
import AppPickup from "~/components/shipping/pickup/AppPickup.vue";
import AppDelivery from "~/components/shipping/delivery/AppDelivery.vue";
import AppGuarantee from "~/components/shipping/guarantee/AppGuarantee.vue";
import AppConditions from "~/components/shipping/conditions/AppConditions.vue";
import AppFeedbackForm from "~/components/FeedbackForm/AppFeedbackForm.vue";

export default {
  name: "Shipping",
  components: {
    AppGuide,
    AppPickup,
    AppDelivery,
    AppGuarantee,
    AppConditions,
    AppFeedbackForm,
  },
};
</script>

<style lang="scss"></style>
