<template>
  <div class="prose mx-auto mt-12">

    <ContentQuery :path="$route.path" find="one" v-slot="{ data }">
      <article>
      <h1 class="mb-20">{{ data.title }}</h1>
      <ContentRenderer :value="data" class="prose" />
      </article>
    </ContentQuery>

<!--    <nuxt-content-->
<!--      :document="page"-->
<!--      class="prose w-full" />-->
  </div>
</template>

<!--<script>-->
<!--export default {-->
<!--  async asyncData({ $content, params, error }) {-->
<!--    let page;-->
<!--    try {-->
<!--      page = await $content("pages", params.slug).fetch();-->
<!--    } catch (e) {-->
<!--      error({ message: "Page not found" });-->
<!--    }-->
<!--    return {-->
<!--      page-->
<!--    };-->
<!--  }-->
<!--};-->
<!--</script>-->
