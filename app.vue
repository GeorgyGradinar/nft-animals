<template>
  <div class="body">
    <HeaderElement></HeaderElement>
    <main>
      <NuxtPage></NuxtPage>
    </main>
  </div>
</template>
<script setup lang="ts">
import HeaderElement from "~/components/HeaderElement.vue";
</script>
<style scoped>
.body {
  background: var(--background);
}
</style>