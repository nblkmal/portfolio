<template>
  <div class="space-y-6">
    <NuxtImg src="/avatar.png" alt="Nabil Akmal"
      class="object-cover ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 bg-gray-200 dark:bg-gray-900 rounded-full h-12 w-12 sm:h-16 sm:w-16"
      sizes="48px sm:64px" placeholder format="webp" />
    <h1 class="text-xl font-bold tracking-tight text-gray-800 dark:text-gray-100">
      Hello!
    </h1>
    <p class="text-gray-900 dark:text-gray-400">
      I'm Nabil Akmal, I'm a Fullstack Software Engineer with 5 years of hands-on coding experience, including 3 amazing years working at RunCloud. I started out mainly on the frontend, but over time I transitioned into a fullstack role. Now I'm just as comfortable building backend services in Laravel as I am crafting clean UIs with Vue and Nuxt.
    </p>
    <p class="text-gray-900 dark:text-gray-400">
      Most of the projects I've worked on followed an end to end approach, so I've been involved in everything from designing system flowcharts and ERDs, mocking up interfaces in Figma, to writing and deploying production-ready code. I also enjoy documenting APIs (I've been using Apicurio Studio recently) and even developed internal SDKs for new service segments in a recent project.
    </p>
      
    <p class="text-gray-900 dark:text-gray-400">
      I've handled a few big features on my own, both frontend and backend, and successfully delivered them without bugs, which I'm pretty proud of. I work mostly with REST APIs, MySQL, and Laravel, and I've been in cloud environments using tools like RunCloud, Cloudflare, and AWS S3.
    </p>
    <p class="text-gray-900 dark:text-gray-400">
      Even though I code full time, I still enjoy designing UI and writing docs. It helps me think through the product as a whole and communicate ideas more clearly. Lately, I've been sharpening my skills in Laravel unit testing and always looking for ways to improve how I build and ship things.
    </p>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-4">My go-to stack are:</h2>
    <div class="flex space-x-3 flex-wrap">
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-laravel"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M3 17l8 5l7 -4v-8l-4 -2.5l4 -2.5l4 2.5v4l-11 6.5l-4 -2.5v-7.5l-4 -2.5z" /><path d="M11 18v4" /><path d="M7 15.5l7 -4" /><path d="M14 7.5v4" /><path d="M14 11.5l4 2.5" /><path d="M11 13v-7.5l-4 -2.5l-4 2.5" /><path d="M7 8l4 -2.5" /><path d="M18 10l4 -2.5" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Laravel</small>
      </div>

      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-vue"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M16.5 4l-4.5 8l-4.5 -8" /><path d="M3 4l9 16l9 -16" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Vue</small>
      </div>

      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-tailwind"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M11.667 6c-2.49 0 -4.044 1.222 -4.667 3.667c.933 -1.223 2.023 -1.68 3.267 -1.375c.71 .174 1.217 .68 1.778 1.24c.916 .912 2 1.968 4.288 1.968c2.49 0 4.044 -1.222 4.667 -3.667c-.933 1.223 -2.023 1.68 -3.267 1.375c-.71 -.174 -1.217 -.68 -1.778 -1.24c-.916 -.912 -1.975 -1.968 -4.288 -1.968zm-4 6.5c-2.49 0 -4.044 1.222 -4.667 3.667c.933 -1.223 2.023 -1.68 3.267 -1.375c.71 .174 1.217 .68 1.778 1.24c.916 .912 1.975 1.968 4.288 1.968c2.49 0 4.044 -1.222 4.667 -3.667c-.933 1.223 -2.023 1.68 -3.267 1.375c-.71 -.174 -1.217 -.68 -1.778 -1.24c-.916 -.912 -1.975 -1.968 -4.288 -1.968z" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Tailwind</small>
      </div>
    </div>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-4">Have a look at my tech stack arsenal below:</h2>
    

    <div class="w-fit bg-gray-200 p-2 rounded-lg">
          <h3 class="uppercase text-xs font-semibold text-gray-600">Frameworks</h3>
    </div>
    <div class="flex space-x-3 flex-wrap">
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-vue"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M16.5 4l-4.5 8l-4.5 -8" /><path d="M3 4l9 16l9 -16" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Vue</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-laravel"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M3 17l8 5l7 -4v-8l-4 -2.5l4 -2.5l4 2.5v4l-11 6.5l-4 -2.5v-7.5l-4 -2.5z" /><path d="M11 18v4" /><path d="M7 15.5l7 -4" /><path d="M14 7.5v4" /><path d="M14 11.5l4 2.5" /><path d="M11 13v-7.5l-4 -2.5l-4 2.5" /><path d="M7 8l4 -2.5" /><path d="M18 10l4 -2.5" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Laravel</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-nuxt"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12.146 8.583l-1.3 -2.09a1.046 1.046 0 0 0 -1.786 .017l-5.91 9.908a1.046 1.046 0 0 0 .897 1.582h3.913" /><path d="M20.043 18c.743 0 1.201 -.843 .82 -1.505l-4.044 -7.013a.936 .936 0 0 0 -1.638 0l-4.043 7.013c-.382 .662 .076 1.505 .819 1.505h8.086z" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Nuxt</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-react"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M6.306 8.711c-2.602 .723 -4.306 1.926 -4.306 3.289c0 2.21 4.477 4 10 4c.773 0 1.526 -.035 2.248 -.102" /><path d="M17.692 15.289c2.603 -.722 4.308 -1.926 4.308 -3.289c0 -2.21 -4.477 -4 -10 -4c-.773 0 -1.526 .035 -2.25 .102" /><path d="M6.305 15.287c-.676 2.615 -.485 4.693 .695 5.373c1.913 1.105 5.703 -1.877 8.464 -6.66c.387 -.67 .733 -1.339 1.036 -2" /><path d="M17.694 8.716c.677 -2.616 .487 -4.696 -.694 -5.376c-1.913 -1.105 -5.703 1.877 -8.464 6.66c-.387 .67 -.733 1.34 -1.037 2" /><path d="M12 5.424c-1.925 -1.892 -3.82 -2.766 -5 -2.084c-1.913 1.104 -1.226 5.877 1.536 10.66c.386 .67 .793 1.304 1.212 1.896" /><path d="M12 18.574c1.926 1.893 3.821 2.768 5 2.086c1.913 -1.104 1.226 -5.877 -1.536 -10.66c-.375 -.65 -.78 -1.283 -1.212 -1.897" /><path d="M11.5 12.866a1 1 0 1 0 1 -1.732a1 1 0 0 0 -1 1.732z" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">React</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-tailwind"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M11.667 6c-2.49 0 -4.044 1.222 -4.667 3.667c.933 -1.223 2.023 -1.68 3.267 -1.375c.71 .174 1.217 .68 1.778 1.24c.916 .912 2 1.968 4.288 1.968c2.49 0 4.044 -1.222 4.667 -3.667c-.933 1.223 -2.023 1.68 -3.267 1.375c-.71 -.174 -1.217 -.68 -1.778 -1.24c-.916 -.912 -1.975 -1.968 -4.288 -1.968zm-4 6.5c-2.49 0 -4.044 1.222 -4.667 3.667c.933 -1.223 2.023 -1.68 3.267 -1.375c.71 .174 1.217 .68 1.778 1.24c.916 .912 1.975 1.968 4.288 1.968c2.49 0 4.044 -1.222 4.667 -3.667c-.933 1.223 -2.023 1.68 -3.267 1.375c-.71 -.174 -1.217 -.68 -1.778 -1.24c-.916 -.912 -1.975 -1.968 -4.288 -1.968z" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Tailwind</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
      <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-golang"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M15.695 14.305c1.061 1.06 2.953 .888 4.226 -.384c1.272 -1.273 1.444 -3.165 .384 -4.226c-1.061 -1.06 -2.953 -.888 -4.226 .384c-1.272 1.273 -1.444 3.165 -.384 4.226z" /><path d="M12.68 9.233c-1.084 -.497 -2.545 -.191 -3.591 .846c-1.284 1.273 -1.457 3.165 -.388 4.226c1.07 1.06 2.978 .888 4.261 -.384a3.669 3.669 0 0 0 1.038 -1.921h-2.427" /><path d="M5.5 15h-1.5" /><path d="M6 9h-2" /><path d="M5 12h-3" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Golang</small>
      </div>
    </div>
    <div class="flex space-x-12">
      <div class="flex flex-col space-y-6">
        <div class="w-fit bg-gray-200 p-2 rounded-lg">
      <h3 class="uppercase text-xs font-semibold text-gray-600">Languages</h3>
    </div>
    <div class="flex space-x-3 flex-wrap">
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-php"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 12m-10 0a10 9 0 1 0 20 0a10 9 0 1 0 -20 0" /><path d="M5.5 15l.395 -1.974l.605 -3.026h1.32a1 1 0 0 1 .986 1.164l-.167 1a1 1 0 0 1 -.986 .836h-1.653" /><path d="M15.5 15l.395 -1.974l.605 -3.026h1.32a1 1 0 0 1 .986 1.164l-.167 1a1 1 0 0 1 -.986 .836h-1.653" /><path d="M12 7.5l-1 5.5" /><path d="M11.6 10h2.4l-.5 3" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">PHP</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-nodejs"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M9 9v8.044a2 2 0 0 1 -2.996 1.734l-1.568 -.9a3 3 0 0 1 -1.436 -2.561v-6.635a3 3 0 0 1 1.436 -2.56l6 -3.667a3 3 0 0 1 3.128 0l6 3.667a3 3 0 0 1 1.436 2.561v6.634a3 3 0 0 1 -1.436 2.56l-6 3.667a3 3 0 0 1 -3.128 0" /><path d="M17 9h-3.5a1.5 1.5 0 0 0 0 3h2a1.5 1.5 0 0 1 0 3h-3.5" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Javascript</small>
      </div>
      
    </div>
      </div>
      <div class="flex flex-col space-y-6">
        <div class="w-fit bg-gray-200 p-2 rounded-lg">
          <h3 class="uppercase text-xs font-semibold text-gray-600">Library Compiler</h3>
        </div>
        <div class="flex space-x-3 flex-wrap">
          <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-yarn"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M17.845 19.308c-1.268 .814 -2.41 1.254 -3.845 1.692c-.176 .21 -.645 .544 -.912 .588a42.469 42.469 0 0 1 -4.498 .412c-.812 .006 -1.31 -.214 -1.447 -.554c-.115 -.279 .336 -2.054 .298 -1.964c-.157 .392 -.575 1.287 -.997 1.72c-.579 .6 -1.674 .4 -2.322 .051c-.71 -.386 -.07 -1.28 -.346 -1.267c-.276 .014 -.776 -1.486 -.776 -2.236c0 -.828 .622 -1.674 1.235 -2.211a6.811 6.811 0 0 1 .46 -3.143a7.414 7.414 0 0 1 2.208 -2.615s-1.353 -1.534 -.849 -2.912c.328 -.902 .46 -.895 .567 -.935c.38 -.12 .727 -.33 1.013 -.612c.78 -.88 1.96 -1.438 3.116 -1.322c0 0 .781 -2.43 1.533 -1.936c.415 .653 .671 1.218 .967 1.936c0 0 1.15 -.7 1.25 -.5c.514 1.398 .487 3.204 .211 4.67c-.324 1.408 -.84 2.691 -1.711 3.83c-.094 .16 .98 .705 1.722 2.812c.686 1.928 .278 2.438 .278 2.688s.716 .144 2.296 -.855a5.848 5.848 0 0 1 2.984 -1.145c.735 -.066 .988 -.035 1.22 1c.232 1.035 -.346 1.406 -.744 1.506c0 0 -2.09 .675 -2.911 1.302z" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Yarn</small>
      </div>

      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-npm"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M1 8h22v7h-12v2h-4v-2h-6z" /><path d="M7 8v7" /><path d="M14 8v7" /><path d="M17 11v4" /><path d="M4 11v4" /><path d="M11 11v1" /><path d="M20 11v4" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">NPM</small>
      </div>
        </div>
      </div>
    </div>
    <div class="flex space-x-12">
      <div class="flex flex-col space-y-6">
        <div class="w-fit bg-gray-200 p-2 rounded-lg">
          <h3 class="uppercase text-xs font-semibold text-gray-600">APIs</h3>
        </div>
        <div class="flex space-x-3 flex-wrap">
          <div class="flex flex-col items-center justify-center space-y-2">
            <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
              <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-api"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M4 13h5" /><path d="M12 16v-8h3a2 2 0 0 1 2 2v1a2 2 0 0 1 -2 2h-3" /><path d="M20 8v8" /><path d="M9 16v-5.5a2.5 2.5 0 0 0 -5 0v5.5" /></svg>
            </div>
            <small class="text-xs text-gray-600 font-semibold">REST API</small>
          </div>
          <div class="flex flex-col items-center justify-center space-y-2">
            <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
              <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-rocket"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M4 13a8 8 0 0 1 7 7a6 6 0 0 0 3 -5a9 9 0 0 0 6 -8a3 3 0 0 0 -3 -3a9 9 0 0 0 -8 6a6 6 0 0 0 -5 3" /><path d="M7 14a6 6 0 0 0 -3 6a6 6 0 0 0 6 -3" /><path d="M15 9m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0" /></svg>
            </div>
            <small class="text-xs text-gray-600 font-semibold">Postman</small>
          </div>
        </div>
      </div>
      <div class="flex flex-col space-y-6">
        <div class="w-fit bg-gray-200 p-2 rounded-lg">
          <h3 class="uppercase text-xs font-semibold text-gray-600">DevOps & Infrastructure</h3>
        </div>
        <div class="flex space-x-3 flex-wrap">
          <div class="flex flex-col items-center justify-center space-y-2">
            <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
              <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-docker"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M22 12.54c-1.804 -.345 -2.701 -1.08 -3.523 -2.94c-.487 .696 -1.102 1.568 -.92 2.4c.028 .238 -.32 1 -.557 1h-14c0 5.208 3.164 7 6.196 7c4.124 .022 7.828 -1.376 9.854 -5c1.146 -.101 2.296 -1.505 2.95 -2.46z" /><path d="M5 10h3v3h-3z" /><path d="M8 10h3v3h-3z" /><path d="M11 10h3v3h-3z" /><path d="M8 7h3v3h-3z" /><path d="M11 7h3v3h-3z" /><path d="M11 4h3v3h-3z" /><path d="M4.571 18c1.5 0 2.047 -.074 2.958 -.78" /><path d="M10 16l0 .01" /></svg>
            </div>
            <small class="text-xs text-gray-600 font-semibold">Docker</small>
          </div>
          <div class="flex flex-col items-center justify-center space-y-2">
            <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
              <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-asterisk"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 12l8 -4.5" /><path d="M12 12v9" /><path d="M12 12l-8 -4.5" /><path d="M12 12l8 4.5" /><path d="M12 3v9" /><path d="M12 12l-8 4.5" /></svg>
            </div>
            <small class="text-xs text-gray-600 font-semibold">Kubernetes</small>
          </div>
        </div>

      </div>
    </div>
    <div class="flex space-x-12">
      <div class="flex flex-col space-y-6">
        <div class="w-fit bg-gray-200 p-2 rounded-lg">
      <h3 class="uppercase text-xs font-semibold text-gray-600">Databases & Storage</h3>
    </div>
    <div class="flex space-x-3 flex-wrap">
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-supabase"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M4 14h8v7l8 -11h-8v-7z" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Supabase</small>
      </div>
      
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-mysql"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M13 21c-1.427 -1.026 -3.59 -3.854 -4 -6c-.486 .77 -1.501 2 -2 2c-1.499 -.888 -.574 -3.973 0 -6c-1.596 -1.433 -2.468 -2.458 -2.5 -4c-3.35 -3.44 -.444 -5.27 2.5 -3h1c8.482 .5 6.421 8.07 9 11.5c2.295 .522 3.665 2.254 5 3.5c-2.086 -.2 -2.784 -.344 -3.5 0c.478 1.64 2.123 2.2 3.5 3" /><path d="M9 7h.01" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">MySQL</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-aws"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M17 18.5a15.198 15.198 0 0 1 -7.37 1.44a14.62 14.62 0 0 1 -6.63 -2.94" /><path d="M19.5 21c.907 -1.411 1.451 -3.323 1.5 -5c-1.197 -.773 -2.577 -.935 -4 -1" /><path d="M3 11v-4.5a1.5 1.5 0 0 1 3 0v4.5" /><path d="M3 9h3" /><path d="M9 5l1.2 6l1.8 -4l1.8 4l1.2 -6" /><path d="M18 10.25c0 .414 .336 .75 .75 .75h1.25a1 1 0 0 0 1 -1v-1a1 1 0 0 0 -1 -1h-1a1 1 0 0 1 -1 -1v-1a1 1 0 0 1 1 -1h1.25a.75 .75 0 0 1 .75 .75" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">AWS S3</small>
      </div>
    </div>
      </div>
      <div class="flex flex-col space-y-6">
        <div class="w-fit bg-gray-200 p-2 rounded-lg">
      <h3 class="uppercase text-xs font-semibold text-gray-600">Development Tools</h3>
    </div>
    <div class="flex space-x-3 flex-wrap">
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-cloudflare"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M13.031 7.007c2.469 -.007 3.295 1.293 3.969 2.993c4 0 4.994 3.825 5 6h-20c-.001 -1.64 1.36 -2.954 3 -3c0 -1.5 1 -3 3 -3c.66 -1.942 2.562 -2.986 5.031 -2.993z" /><path d="M12 13h6" /><path d="M17 10l-2.5 6" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Cloudflare</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-figma"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M15 12m-3 0a3 3 0 1 0 6 0a3 3 0 1 0 -6 0" /><path d="M6 3m0 3a3 3 0 0 1 3 -3h6a3 3 0 0 1 3 3v0a3 3 0 0 1 -3 3h-6a3 3 0 0 1 -3 -3z" /><path d="M9 9a3 3 0 0 0 0 6h3m-3 0a3 3 0 1 0 3 3v-15" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Figma</small>
      </div>
    </div>
      </div>
    </div>
    
    <div class="w-fit bg-gray-200 p-2 rounded-lg">
      <h3 class="uppercase text-xs font-semibold text-gray-600">Security & Authentication</h3>
    </div>
    <div class="flex space-x-3 flex-wrap">
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-fish"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M16.69 7.44a6.973 6.973 0 0 0 -1.69 4.56c0 1.747 .64 3.345 1.699 4.571" /><path d="M2 9.504c7.715 8.647 14.75 10.265 20 2.498c-5.25 -7.761 -12.285 -6.142 -20 2.504" /><path d="M18 11v.01" /><path d="M11.5 10.5c-.667 1 -.667 2 0 3" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Wireshark</small>
      </div>
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-access-point"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 12l0 .01" /><path d="M14.828 9.172a4 4 0 0 1 0 5.656" /><path d="M17.657 6.343a8 8 0 0 1 0 11.314" /><path d="M9.168 14.828a4 4 0 0 1 0 -5.656" /><path d="M6.337 17.657a8 8 0 0 1 0 -11.314" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Burpsuite</small>
      </div>
    </div>
    
    <div class="w-fit bg-gray-200 p-2 rounded-lg">
      <h3 class="uppercase text-xs font-semibold text-gray-600">Documentation & Ticketing</h3>
    </div>
    <div class="flex space-x-3 flex-wrap">
      <div class="flex flex-col items-center justify-center space-y-2">
        <div class="flex items-center justify-center ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 rounded-full p-1">
          <svg  xmlns="http://www.w3.org/2000/svg"  width="38"  height="38"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="1.5"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-bitbucket"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M3.648 4a.64 .64 0 0 0 -.64 .744l3.14 14.528c.07 .417 .43 .724 .852 .728h10a.644 .644 0 0 0 .642 -.539l3.35 -14.71a.641 .641 0 0 0 -.64 -.744l-16.704 -.007z" /><path d="M14 15h-4l-1 -6h6z" /></svg>
        </div>
        <small class="text-xs text-gray-600 font-semibold">Atlassian</small>
        <small class="text-xs text-gray-600 font-semibold">(Jira, Confluence, Bitbucket)</small>
      </div>
    </div>

    <!-- <p class="text-gray-900 dark:text-gray-400">
      By day, I'm a Fullstack Developer at
      <a href="https://headshotpro.com" target="_blank" class="underline">Headshotpro</a>, and
      by night (and weekends), I'm busy tinkering with some random tool or app
      that I am building.
    </p> -->
  </div>
</template>

<script setup>
useSeoMeta({
  title: "Nabil Akmal",
  description:
    "I'm Nabil Akmal, your friendly neighborhood software, product engineer and designer from Bengaluru, India. I specialize in building web applications and sites using Javascript, React, Vue & Node.",
});
</script>
