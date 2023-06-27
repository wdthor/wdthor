<template>
  <main>
    <div>
      <h1>Oops</h1>
      <BaseButton>Go back to homepage</BaseButton>
    </div>
  </main>
</template>

<script setup lang="ts">
import BaseButton from '@/components/base/BaseButton.vue'
</script>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  margin-top: 1rem;
}
</style>
