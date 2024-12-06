<script setup lang="ts">
import { proseHeadingClick } from '~/utils'

const props = defineProps<{
  id?: string
}>()

</script>

<template>
  <h3 :id>
    <slot />
    <sub style="color: red;">custom</sub>
  </h3>
</template>
