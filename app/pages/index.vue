<template>
  <div class="prose mx-auto mt-12">
    <h1 class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-3xl pb-12">
      {{ page.title }}
    </h1>
    <ContentDoc path="/home" class="prose w-full" />
  </div>
</template>

<script setup>
const { data: page } = await useAsyncData('home', () => queryContent('home').findOne())
</script>
