<script setup lang="ts">
const route = useRoute();
console.log(route.path);
const { data } = await useAsyncData(() =>
  queryCollection('content').path(route.path).first()
);
</script>

<template>
  <div>
    <div>{{ route.path }}</div>
    <ContentRenderer v-if="data" :value="data" />
    <div v-else>Page not found</div>
  </div>
</template>
