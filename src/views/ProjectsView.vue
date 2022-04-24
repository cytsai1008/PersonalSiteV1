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
        <div class="ts-grid is-stackable is-2-columns">
          <div class="ts-column">
            <div class="ts-image is-rounded is-2-by-1 is-covered">
              <div class="ts-placeholder is-loading is-rounded">
                <div class="image" style="width: 250px; height: 125px">
                  <img
                    :src="generateSRC('PixelGameMaker', 'PixelRPG-Python')"
                    style="max-width: 250px"
                  />
                </div>
              </div>
            </div>
          </div>
          <div class="ts-column">
            <div class="ts-container is-fluid">
              <div class="ts-header is-heavy is-large">PixelRPG-Python</div>
            </div>
          </div>
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

.gh-column:hover {
  transform: scale(1.5);
  z-index: 999;
  box-shadow: 5px 5px 5px #aaaaaa;
  border-radius: 0.4rem !important;
}
RouterLink {
  color: inherit;
  text-decoration: none;
}
</style>
