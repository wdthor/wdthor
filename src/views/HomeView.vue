<template>
  <main>
    <h1>Hey there, I'm wdthor</h1>
    <BaseButton @click="goToProjects">Go to projects</BaseButton>
  </main>
</template>

<script setup lang="ts">
import BaseButton from '@/components/base/BaseButton.vue'

import { useRouter } from 'vue-router'

const router = useRouter()

const goToProjects = () => router.push({ name: 'Project1' })
</script>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  margin-top: 1rem;
}
</style>
