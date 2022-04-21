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
    <div class="ts-divider is-section"></div>
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
    <div class="ts-container is-fluid is-narrow" id="Projs">
      <div class="ts-center">
        <div class="ts-space"></div>
        <div class="ts-header is-heavy is-large is-start-icon">
          Below is some of my
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
        <div class="ts-header is-heavy is-big"></div>
      </div>
    </div>
  </main>
</template>

<style>
#Introduce {
  width: 100vw;
  /*
  background-color: #14439b;
  */
}
</style>
