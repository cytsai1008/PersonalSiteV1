<script setup>
/*
import TheWelcome from "@/components/TheWelcome.vue";
*/
import { Head } from "@vueuse/head";
</script>

<script>
// generate random number
function randomNumber(min, max) {
  return Math.floor(Math.random() * (max - min + 1) + min);
}

function generateSRC(UserName, Repo) {
  const randomNum = randomNumber(10000000, 1000000000000);
  return (
    "https://opengraph.githubassets.com/" +
    randomNum +
    "/" +
    UserName +
    "/" +
    Repo
  );
}
</script>

<template>
  <Head>
    <title>Projects</title>
  </Head>
  <main>
    <div class="ts-container is-fluid" id="Repos">
      <div class="ts-center">
        <div class="ts-space"></div>
        <div class="ts-header is-heavy is-large" style="text-align: center">
          My Repositories
        </div>
        <div class="ts-space is-small"></div>
        <div class="ts-divider is-section" id="about-proj-divider"></div>
        <div class="ts-space is-small"></div>
        <!-- box -->
      </div>
    </div>
    <div class="container mx-auto">
      <!-- tailwind grid -->
      <div
        class="mt-6 space-y-12 lg:space-y-0 lg:grid lg:grid-cols-3 lg:gap-x-6"
      >
        <div class="group relative">
          <div
            class="relative w-full h-80 bg-white rounded-lg overflow-hidden group-hover:opacity-75 sm:aspect-w-2 sm:aspect-h-1 sm:h-64 lg:aspect-w-1 lg:aspect-h-1"
          >
            <img
              :src="generateSRC('PixelGameMaker', 'PixelRPG-Python')"
              class="w-full h-full object-center object-cover"
              alt="GitHub Badges"
            />
          </div>
          <h3 class="mt-6 text-sm text-gray-500">Name</h3>
          <p class="text-base font-semibold text-gray-900">Description</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style>
#Repos {
  width: 100vw;
}

#about-proj-divider {
  width: 100vw;
}

/*
.gh-box-img {
  width: 450px;
  height: 225px;
}

@media only screen and (max-width: 768px) {
  // CSS that should be displayed if width is equal to or less than 800px goes here
  .gh-box-img {
    width: auto;
    height: auto;
    max-width: 450px !important;
    max-height: 225px !important;
  }
}
*/
RouterLink {
  color: inherit !important;
  text-decoration: none !important;
}

.ts-box {
  transition: box-shadow 0.3s;
  float: left;
}

.ts-box:hover {
  box-shadow: 0 0 15px #aaaaaa;
}

.container {
  padding: 2rem;
}
</style>
