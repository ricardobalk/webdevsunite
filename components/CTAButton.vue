<template>
  <NuxtLink class="button" :to="link">
    <slot />
  </NuxtLink>
</template>

<style lang="scss">
.button {
  @apply rounded-full px-4 py-3 bg-slate-600 text-white hover:bg-slate-800;
}
</style>

<script setup lang="ts">
defineProps({
  link: {
    type: String,
    required: true,
    default: '/',
  }
})
</script>