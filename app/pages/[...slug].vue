<template>
    <ContentQuery :path="$route.path" find="one" v-slot="{ data }">
      <article class="prose mx-auto mt-12">
        <h1 class="mb-20">{{ data.title }}</h1>
        <ContentRenderer :value="data"/>
      </article>
    </ContentQuery>
</template>
