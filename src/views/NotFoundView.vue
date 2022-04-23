<script setup>
import { Head } from "@vueuse/head";
</script>
<template>
  <Head>
    <title>Page Not Found</title>
  </Head>
  <main>
    <div class="ts-container is-fluid is-narrow" id="NotFound">
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
        <div class="ts-header is-heavy is-massive">404</div>
        <div class="ts-space is-small"></div>
        <div class="ts-header is-heavy is-big">Page Not Found</div>
        <div class="ts-space is-small"></div>
        <RouterLink to="/" style="text-decoration: none; color: inherit">
          <div class="ts-text is-heavy is-undecorated">Go Home</div>
        </RouterLink>
      </div>
    </div>
  </main>
</template>
