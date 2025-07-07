<template>
  <main class="min-h-screen">
    <AppHeader class="mb-8" title="Community" :description="description" />
    <ul class="space-y-2">
      <li v-for="bookmark in bookmarks" :key="bookmark.id">
        
        <a
          :href="bookmark.url"
          target="_blank"
          class="flex items-center gap-3 hover:bg-gray-100 dark:hover:bg-white/10 p-2 rounded-lg -m-2 text-sm min-w-0"
        >
        <div class="border w-fit bg-white rounded-full p-2">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="currentColor"  class="icon icon-tabler icons-tabler-filled icon-tabler-microphone"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M19 9a1 1 0 0 1 1 1a8 8 0 0 1 -6.999 7.938l-.001 2.062h3a1 1 0 0 1 0 2h-8a1 1 0 0 1 0 -2h3v-2.062a8 8 0 0 1 -7 -7.938a1 1 0 1 1 2 0a6 6 0 0 0 12 0a1 1 0 0 1 1 -1m-7 -8a4 4 0 0 1 4 4v5a4 4 0 1 1 -8 0v-5a4 4 0 0 1 4 -4" /></svg>
        </div>
          <!-- <UAvatar
            :src="getThumbnail(bookmark.url)"
            :alt="bookmark.label"
            :ui="{ rounded: 'rounded-md' }"
          /> -->
          <div class="flex flex-col">
            <p class="truncate font-semibold text-gray-700 dark:text-gray-200">
              {{ bookmark.label }}
            </p>
            <p class="text-xs font-medium text-gray-500 dark:text-gray-200">
            {{ bookmark.role }} @ {{ bookmark.host }} | {{ bookmark.date }}
            </p>
          </div>
          
          <span class="flex-1"></span>
          <!-- <span class="text-xs font-medium text-gray-400 dark:text-gray-600">
            {{ getHost(bookmark.url) }}
          </span> -->
        </a>
      </li>
    </ul>
  </main>
</template>

<script setup>
const description =
  "Community is a collection of resources and tools that I've found useful and want to share with others.";
useSeoMeta({
  title: "Community | Nabil Akmal",
  description,
});

const bookmarks = [
  {
    id: 1,
    label: "Ignite Your Passion: Frontend Software Engineer",
    date: "25 March 2024",
    role: "Speaker",
    host: "Krenovator",
    url: "",
  },
  {
    id: 2,
    label: "Mini Project: Utilised Public APIs",
    date: "12 September 2024",
    role: "Speaker",
    host: "Krenovator",
    url: "",
  },
  {
    id: 3,
    label: "Leveling Up Your Technical Skills: Continuous Learning Strategies",
    date: "21 November 2024",
    role: "Speaker",
    host: "Krenovator",
    url: "",
  },
  {
    id: 4,
    label: "Crack the Code: Are You Ready for a Programming Job?",
    date: "14 January 2025",
    role: "Speaker",
    host: "Krenovator",
    url: "",
  },
  {
    id: 5,
    label: "Student to Tech Pro: Tips They Don't Tell Teach in Class",
    date: "30 May 2025",
    role: "Speaker",
    host: "Krenovator",
    url: "",
  },
];

function getHost(url) {
  const parsedUrl = new URL(url);
  let host = parsedUrl.host;
  if (host.startsWith("www.")) {
    host = host.substring(4);
  }
  return host;
}

function getThumbnail(url) {
  const host = getHost(url);
  return `https://logo.clearbit.com/${host}`;
}
</script>
