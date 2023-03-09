<script>
export default {
  name: "Button",
  props: {
    title: {
      type: String,
      required: true,
    },
    onClick: {
      type: Function,
      required: true,
    },
  },
};
</script>

<template>
  <button class="button" @click="onClick">
    <span class="button__title">{{ title }}</span>
  </button>
</template>

<style lang="scss"></style>
