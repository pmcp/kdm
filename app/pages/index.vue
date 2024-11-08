<template>
  <div class="prose mx-auto mt-12">
    <h1 class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-3xl pb-12">
      {{ page.title }}
    </h1>
    <nuxt-link to="t-i-c">T I C</nuxt-link>
<!--    <ContentDoc path="/pages/home" class="prose w-full" />-->

<!--    <nuxt-content-->
<!--      :document="page"-->
<!--      class="prose w-full" />-->
  </div>
</template>

<script setup>
const { data: page } = await useAsyncData('home', () => queryContent('pages/home').findOne())
</script>
