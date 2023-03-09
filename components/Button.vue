<script>
export default {
  name: "Button",
  props: ["title", "click"],
  emit: ["click"],
};
</script>

<template>
  <button class="button" @click="click">
    <span class="button__title">{{ title }}</span>
  </button>
</template>

<style lang="scss"></style>
