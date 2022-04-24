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
        <RouterLink
          to="/projects/PRPG-PY"
          style="color: inherit !important; text-decoration: none !important"
        >
          <div class="ts-box">
            <div class="ts-image gh-box-img">
              <div class="ts-placeholder is-loading is-rounded">
                <div class="image gh-box-img">
                  <img
                    :src="generateSRC('PixelGameMaker', 'PixelRPG-Python')"
                  />
                </div>
              </div>
            </div>
            <div class="ts-content">
              <div class="ts-header is-heavy">PixelRPG-Python</div>
              <p>A Pixel Art Game Based on PyGame Engine and PySide2</p>
            </div>
          </div>
        </RouterLink>
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

.gh-box-img {
  width: 450px;
  height: 225px;
}

@media only screen and (max-width: 768px) {
  /* CSS that should be displayed if width is equal to or less than 800px goes here */
  .gh-box-img {
    width: auto;
    height: auto;
    max-width: 450px !important;
    max-height: 225px !important;
  }
}

RouterLink {
  color: inherit !important;
  text-decoration: none !important;
}
</style>
