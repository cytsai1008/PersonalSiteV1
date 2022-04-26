<script setup>
/*
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "@/components/HelloWorld.vue";
*/
//import "tocas/dist/tocas.min.css";
//import "tocas/dist/tocas.min.js";
// import { Head } from "@vueuse/head";
</script>

<!--
<script>
import { defineComponent, computed, reactive } from "vue";
import { useHead } from "@vueuse/head";
export default defineComponent({
  setup() {
    const siteData = reactive({
      title: `My website`,
      description: `My beautiful website`,
    });

    useHead({
      // Can be static or computed
      title: computed(() => siteData.title),
      meta: [
        {
          name: `description`,
          content: computed(() => siteData.description),
        },
      ],
    });
  },
});
</script>
-->

<script>
import { useRoute } from "vue-router";
// import { computed } from "vue";
export default {
  computed: {
    currentHomePathText() {
      const route = useRoute();
      return route.path === "/" ? "" : "Home";
    },
    currentHomePathActive() {
      const route = useRoute();
      return route.path === "/" ? "is-active" : "";
    },
    currentProjPathText() {
      const route = useRoute();
      return route.path.includes("/projects") ? "" : "Projects";
    },
    currentProjPathActive() {
      const route = useRoute();
      return route.path.includes("/projects") ? "is-active" : "";
    },
    currentAboutPathText() {
      const route = useRoute();
      return route.path.includes("/about") ? "" : "About";
    },
    currentAboutPathActive() {
      const route = useRoute();
      return route.path.includes("/about") ? "is-active" : "";
    },
  },
};
</script>

<template>
  <!--
  <Head>
    <title>Main</title>
  </Head>
  -->
  <header>
    <!--
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
    -->
    <nav>
      <div class="ts-space is-small"></div>
      <div class="ts-container">
        <div class="ts-row is-relaxed is-evenly-divided is-center-aligned">
          <div class="ts-tab is-center-aligned">
            <!-- ts-app-navbar is-unlabeled -->
            <RouterLink to="/" style="text-decoration: none; color: inherit">
              <a class="item" v-bind:class="currentHomePathActive">
                <span class="ts-icon is-house-icon">
                  <!--Why house regular icon is paid QAQ-->
                </span>
                {{ currentHomePathText }}
              </a>
            </RouterLink>
            <RouterLink
              to="/projects"
              style="text-decoration: none; color: inherit"
            >
              <a class="item" v-bind:class="currentProjPathActive">
                <span class="ts-icon is-file-code-icon"></span>
                {{ currentProjPathText }}
              </a>
            </RouterLink>
            <RouterLink
              to="/about"
              style="text-decoration: none; color: inherit"
            >
              <a class="item" v-bind:class="currentAboutPathActive">
                <span class="ts-icon is-circle-info-icon">
                  <!--Paid icon too... -->
                </span>
                {{ currentAboutPathText }}
              </a>
            </RouterLink>
          </div>
        </div>
      </div>
    </nav>
  </header>
  <div class="ts-container is-fluid">
    <div class="ts-center">
      <RouterView />
    </div>
  </div>
  <div class="ts-space is-large"></div>
  <footer>
    <div class="ts-center">
      <div class="ts-meta is-center-aligned">
        <div class="item">
          ©
          <a
            href="https://www.github.com/cytsai1008"
            target="_blank"
            class="ts-text is-undecorated"
            >CYTsai</a
          >
          2022
        </div>
        <div class="item">
          <a
            href="https://www.github.com/cytsai1008/cytsai1008.github.io"
            target="_blank"
            class="ts-text is-undecorated"
            >Source Code</a
          >
        </div>
        <div class="item">
          Powered by
          <a
            href="https://v4.tocas-ui.com"
            target="_blank"
            class="ts-text is-undecorated is-external-link"
            >Tocas UI</a
          >
        </div>
      </div>
    </div>
  </footer>
</template>
<!--
<style>
.logo {
  margin-bottom: 1rem;
}
.wrapper {
  max-width: 600px;
  margin: 0 auto;
}
.nav {
  margin-top: 1rem;
}
.nav a {
  margin-right: 1rem;
}
</style>
-->
<!--
<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
-->

<style>
header {
  background-color: var(--ts-gray-100);
}
footer {
  background-color: var(--ts-gray-100);
  height: 5.5rem;
}
RouterLink {
  color: inherit;
  text-decoration: none;
}
</style>
<!--
https://stackoverflow.com/questions/53334384/how-to-make-fixed-navbar-with-vue-js
-->
