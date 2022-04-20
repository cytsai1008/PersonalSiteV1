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
    <div class="ts-container is-fluid is-narrow">
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
  </main>
</template>
