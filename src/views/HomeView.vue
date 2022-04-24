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
    <title>Home</title>
  </Head>
  <main>
    <!--
    <TheWelcome />
    -->
    <!--<div class="ts-divider is-section"></div>-->
    <div class="ts-container is-fluid is-narrow" id="Introduce">
      <div class="ts-center">
        <div class="ts-space is-big"></div>
        <div class="ts-placeholder is-loading">
          <div class="image" style="border-radius: 100rem">
            <div class="ts-image is-circular is-small">
              <img src="../assets/sk-head.png" />
            </div>
          </div>
        </div>
        <div class="ts-space"></div>
        <div class="ts-header is-heavy is-massive">Hi, I'm CYTsai</div>
        <div class="ts-space is-small"></div>
        <div class="ts-header is-heavy is-big" style="text-align: center">
          A high school student / Amateur programmer
        </div>
      </div>
    </div>
    <div class="ts-divider is-section" id="about-proj-divider"></div>
    <div class="ts-container is-fluid is-narrow" id="Repos">
      <div class="ts-center">
        <div class="ts-space"></div>
        <div class="ts-header is-heavy is-large" style="text-align: center">
          My Mainly Contributed Repositories
        </div>
        <div class="ts-space is-large"></div>
        <div class="ts-grid is-stackable is-2-columns">
          <div class="column">
            <RouterLink to="/projects/PRPG-PY">
              <div class="ts-image is-rounded is-2-by-1 is-covered gh-column">
                <div class="ts-placeholder is-loading is-rounded">
                  <div class="image" style="width: 250px; height: 125px">
                    <img
                      :src="generateSRC('PixelGameMaker', 'PixelRPG-Python')"
                      style="max-width: 250px"
                    />
                  </div>
                </div>
              </div>
            </RouterLink>
          </div>
          <div class="column">
            <RouterLink to="/projects/WFNM">
              <div class="ts-image is-rounded is-2-by-1 is-covered gh-column">
                <div class="ts-placeholder is-loading is-rounded">
                  <div class="image" style="width: 250px; height: 125px">
                    <img
                      :src="generateSRC('cytsai1008', 'What-For-Next-Meal')"
                      style="max-width: 250px"
                    />
                  </div>
                </div>
              </div>
            </RouterLink>
          </div>

          <div class="column">
            <RouterLink to="/projects/DV">
              <div class="ts-image is-rounded is-2-by-1 is-covered gh-column">
                <div class="ts-placeholder is-loading is-rounded">
                  <div class="image" style="width: 250px; height: 125px">
                    <img
                      :src="generateSRC('cytsai1008', 'DiscordVoice')"
                      style="max-width: 250px"
                    />
                  </div>
                </div>
              </div>
            </RouterLink>
          </div>
          <div class="column">
            <RouterLink to="/projects/GH-Pages">
              <div class="ts-image is-rounded is-2-by-1 is-covered gh-column">
                <div class="ts-placeholder is-loading is-rounded">
                  <div class="image" style="width: 250px; height: 125px">
                    <img
                      :src="generateSRC('cytsai1008', 'cytsai1008.github.io')"
                      style="max-width: 250px"
                    />
                  </div>
                </div>
              </div>
            </RouterLink>
          </div>
        </div>
        <div class="ts-space is-big"></div>
        <div class="ts-header is-heavy is-large">
          For more projects please visit
        </div>
        <div class="ts-space is-small"></div>
        <div class="ts-header is-heavy is-large is-start-icon">
          <RouterLink
            to="/projects"
            style="text-decoration: none; color: inherit"
          >
            <div class="ts-text is-undecorated">
              <span class="ts-icon is-file-code-icon"></span>
              Projects
            </div>
          </RouterLink>
        </div>
        <div class="ts-header is-heavy is-large is-start-icon">
          <a
            href="http://www.github.com/cytsai1008"
            class="ts-text is-undecorated is-external-link"
            target="_blank"
            ><span class="ts-icon is-github-icon"></span>GitHub Repos
          </a>
        </div>
      </div>
    </div>
  </main>
</template>

<style>
#Introduce {
  width: 100vw;
}

#about-proj-divider {
  width: 100vw;
}

.gh-column {
  transition: box-shadow 0.3s;
  transition: transform 0.2s;
  float: left;
}

.gh-column:hover {
  transform: scale(1.2);
  z-index: 999;
  box-shadow: 0 0 15px #aaaaaa;
  border-radius: 0.4rem !important;
}
RouterLink {
  color: inherit;
  text-decoration: none;
}
</style>
