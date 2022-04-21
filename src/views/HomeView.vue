<script setup>
/*
import TheWelcome from "@/components/TheWelcome.vue";
*/
import { Head } from "@vueuse/head";
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
        <div class="ts-image is-circular is-small">
          <img src="../assets/sk-head.png" />
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
        <div class="ts-grid is-evenly-divided is-stackable">
          <div class="column">
            <div class="ts-image is-rounded is-2-by-1 is-covered">
              <img
                src="https://opengraph.githubassets.com/8c7ac0246ac7497315ae5018b49d3aadefdf62df6d576cb8181b4181e03cd1b2/PixelGameMaker/PixelRPG-Python"
                style="max-width: 250px"
              />
            </div>
          </div>
          <div class="column">
            <div class="ts-image is-rounded is-2-by-1 is-covered">
              <img
                src="https://opengraph.githubassets.com/18922ec22639cd55ecd602ee8382bae770e5f4d4a2b2ad210a2875d351efd36b/cytsai1008/What-For-Next-Meal"
                style="max-width: 250px"
              />
            </div>
          </div>

          <div class="column">
            <div class="ts-image is-rounded is-2-by-1 is-covered">
              <img
                src="https://opengraph.githubassets.com/d1d9c2d8f1a3adc38087a9bf384d8e5c8e06dca112d73e76d9b6f40283f1de19/cytsai1008/DiscordVoice"
                style="max-width: 250px"
              />
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
