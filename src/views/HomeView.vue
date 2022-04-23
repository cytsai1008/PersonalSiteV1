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
        <div class="ts-header is-heavy is-big">
          A high school student / <br />
          Amateur programmer
        </div>
      </div>
    </div>
    <div class="ts-divider is-section"></div>
    <div class="ts-container is-fluid is-narrow" id="Repos">
      <div class="ts-center">
        <div class="ts-space"></div>
        <div class="ts-grid is-stackable">
          <div class="column is-5-wide">
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
          <div class="column is-5-wide">
            <div class="ts-image is-rounded is-2-by-1 is-covered">
              <div class="ts-placeholder is-loading is-rounded">
                <div class="image" style="width: 250px; height: 125px">
                  <img
                    :src="generateSRC('cytsai1008', 'What-For-Next-Meal')"
                    style="max-width: 250px"
                  />
                </div>
              </div>
            </div>
          </div>

          <div class="column is-5-wide">
            <div class="ts-image is-rounded is-2-by-1 is-covered">
              <div class="ts-placeholder is-loading is-rounded">
                <div class="image" style="width: 250px; height: 125px">
                  <img
                    :src="generateSRC('cytsai1008', 'DiscordVoice')"
                    style="max-width: 250px"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="ts-space"></div>
        <div class="ts-header is-heavy is-large">
          for more projects please visit my
        </div>
        <div class="ts-header is-heavy is-large is-start-icon">
          <a
            href="http://www.github.com/cytsai1008"
            class="ts-text is-undecorated is-external-link"
            target="_blank"
            ><span class="ts-icon is-github-icon"></span>GitHub Repos
          </a>
        </div>
        <div class="ts-space is-small"></div>
      </div>
    </div>
  </main>
</template>

<style>
#Introduce {
  width: 100vw;
}
</style>
