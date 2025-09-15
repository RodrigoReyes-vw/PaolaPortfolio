<script setup lang="ts">
const route = useRoute()


const { data } = await useAsyncData(() => queryCollection('content').path(route.path).first())

</script>
<template>
    <h1 class="text-6xl">{{ data?.title }}</h1>
    <pre class="">{{ data?.meta.date }}</pre>
    
    <ContentRenderer :value="data" />
</template>
<style scoped></style>