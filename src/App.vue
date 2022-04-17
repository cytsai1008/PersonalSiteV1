<script setup>
/*
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "@/components/HelloWorld.vue";
*/
import "tocas/dist/tocas.min.css";
import "tocas/dist/tocas.min.js";
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
      return route.path === "/" ? " " : " Home ";
    },
    currentHomePathActive() {
      const route = useRoute();
      return route.path === "/" ? "is-active" : "";
    },
    currentProjPathText() {
      const route = useRoute();
      return route.path === "/projects" ? " " : " Projects ";
    },
    currentProjPathActive() {
      const route = useRoute();
      return route.path === "/projects" ? "is-active" : "";
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
      <div class="ts-container">
        <div class="ts-row is-relaxed is-evenly-divided is-center-aligned">
          <div class="ts-tab is-center-aligned is-secondary">
            <RouterLink to="/">
              <a class="item" v-bind:class="currentHomePathActive">
                <span class="ts-icon is-house-icon"></span>
                {{ currentHomePathText }}
              </a>
            </RouterLink>
            <RouterLink to="/projects">
              <a class="item" v-bind:class="currentProjPathActive">
                <span class="ts-icon is-file-code-icon"></span>
                {{ currentProjPathText }}
              </a>
            </RouterLink>
          </div>
        </div>
      </div>
    </nav>
  </header>

  <RouterView />
</template>
<style></style>
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
