<template>
  <main class="content">
    <slot></slot>
  </main>
</template>

<script>
export default {
  name: "AppContent",
};
</script>

<style>
.content {
  position: relative;
  flex: 1 0 auto;
  width: 100vw;
  max-width: 100%;
}
</style>
