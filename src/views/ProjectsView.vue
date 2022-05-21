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
    <div class="ts-container is-fluid">
      <div class="ts-center">
        <div class="ts-grid is-stackable">
          <!-- https://bootcamp.uxdesign.cc/embed-your-github-project-on-your-react-website-ccefacc30f62 -->
          <RouterLink to="/projects/PRPG-PY" class="column is-8-wide">
            <!--
            <img
              :src="generateSRC('PixelGameMaker', 'PixelRPG-Python')"
              style="border-radius: 0.5rem"
              alt="GitHub Repo Card"
            />
            -->
            <img
              src="https://gh-card.dev/repos/PixelGameMaker/PixelRPG-Python.svg?fullname="
              class="gh-card gh-box-shadow"
              style="border-radius: 0.5rem"
              alt="GitHub Repo Card"
            />
          </RouterLink>
          <RouterLink to="/projects/DV" class="column is-8-wide">
            <img
              src="https://gh-card.dev/repos/cytsai1008/DiscordVoice.svg?fullname="
              class="gh-card gh-box-shadow"
              style="border-radius: 0.5rem"
              alt="GitHub Repo Card"
            />
          </RouterLink>
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

.gh-box-shadow {
  transition: box-shadow 0.3s;
  float: left;
}

.gh-box-shadow:hover {
  box-shadow: 0 0 15px #aaaaaa;
}

@media (prefers-color-scheme: dark) {
  .gh-card {
    filter: invert(80%);
  }
}
</style>
