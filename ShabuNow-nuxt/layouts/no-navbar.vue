<script lang="ts" setup></script>

<template>
  <section>
    <slot />
  </section>
</template>

<style scoped>
* {
  font-family: "Kanit", sans-serif;
}
</style>

<script>
export default {
  layout: 'no-navbar'
}
</script>
