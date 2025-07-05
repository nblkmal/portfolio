<template>
  <div class="space-y-6">
    <NuxtImg src="/circle-profile.png" alt="Nabil Akmal"
      class="object-cover ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 bg-gray-200 dark:bg-gray-900 rounded-full h-12 w-12 sm:h-16 sm:w-16"
      sizes="48px sm:64px" placeholder format="webp" />
    <h1 class="text-xl font-bold tracking-tight text-gray-800 dark:text-gray-100">
      Hello!
    </h1>
    <p class="text-gray-900 dark:text-gray-400">
      I'm Nabil Akmal, I’m a Fullstack Software Engineer with 4 years of hands-on coding experience, including 3 amazing years working at RunCloud. I started out mainly on the frontend, but over time I transitioned into a fullstack role. Now I’m just as comfortable building backend services in Laravel as I am crafting clean UIs with Vue and Nuxt.

Most of the projects I’ve worked on followed an end to end approach, so I’ve been involved in everything from designing system flowcharts and ERDs, mocking up interfaces in Figma, to writing and deploying production-ready code. I also enjoy documenting APIs (I’ve been using Apicurio Studio recently) and even developed internal SDKs for new service segments in a recent project.

I’ve handled a few big features on my own, both frontend and backend, and successfully delivered them without bugs, which I’m pretty proud of. I work mostly with REST APIs, MySQL, and Laravel, and I’ve been in cloud environments using tools like RunCloud, Cloudflare, and AWS S3.

Even though I code full time, I still enjoy designing UI and writing docs. It helps me think through the product as a whole and communicate ideas more clearly. Lately, I’ve been sharpening my skills in Laravel unit testing and always looking for ways to improve how I build and ship things.
    </p>
    <p class="text-gray-900 dark:text-gray-400">
      By day, I'm a Fullstack Developer at
      <a href="https://headshotpro.com" target="_blank" class="underline">Headshotpro</a>, and
      by night (and weekends), I'm busy tinkering with some random tool or app
      that I am building.
    </p>
  </div>
</template>

<script setup>
useSeoMeta({
  title: "Nabil Akmal",
  description:
    "I'm Nabil Akmal, your friendly neighborhood software, product engineer and designer from Bengaluru, India. I specialize in building web applications and sites using Javascript, React, Vue & Node.",
});
</script>
