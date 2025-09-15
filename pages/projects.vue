<template>
  <main class="min-h-screen">
    <AppHeader class="mb-12" title="Projects" :description="description" />
    <div class="space-y-4">
      <AppProjectCard
      v-for="(project, id) in projects"
      :key="id"
      :project="project"
      />
    </div>
    <AppHeader class="my-12" title="Open Source Contributions" description="I challenged myself to contribute to open source projects to improve my skills and help the community." />
    <div class="space-y-4">
      <AppProjectCard
      v-for="(contribution, id) in contributions"
      :key="id"
      :project="contribution"
      />
    </div>
  </main>
</template>

<script setup>
const description =
  "Here are some of the projects I've worked on. Some of them are not working (LOL), but I'm still proud of them.";
useSeoMeta({
  title: "Projects | Nabil Akmal",
  description,
});

const { data: projects } = await useAsyncData("projects-all", () => queryContent("/projects").find());
const { data: contributions } = await useAsyncData("contributions-all", () => queryContent("/contributions").find());
</script>
