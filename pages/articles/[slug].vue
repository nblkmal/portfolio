<template>
  <main class="min-h-screen">
    <div
      class="prose dark:prose-invert prose-blockquote:not-italic prose-pre:bg-gray-900 prose-img:ring-1 prose-img:ring-gray-200 dark:prose-img:ring-white/10 prose-img:rounded-lg"
    >
      <ContentDoc v-slot="{ doc }" tag="article">
        <div class="mb-8">
          <ULink to="/articles" class="text-sm text-amber-600 no-underline">Articles</ULink>
          <span class="mx-2">/</span>
          <span class="text-sm text-gray-500">{{ doc.title }}</span>
        </div>
        <article>
          <h1>{{ doc.title }}</h1>
          <ContentRenderer :value="doc" />
        </article>
      </ContentDoc>
    </div>
  </main>
</template>
<script setup>
const route = useRoute();
const { slug } = route.params;
useSeoMeta({
  ogImage: `/avatar.png`,
  twitterCard: "summary_large_image",
  articleAuthor: "Nabil Akmal",
});
</script>
<style>
.prose h2 a,
.prose h3 a {
  @apply no-underline;
}
</style>
