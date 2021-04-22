<template>
  <div class="">
    <AppHeader />
    <main class="main">
      <section class="section__text section__text--left">
        <app-text-header
          class="text__header--left"
          content="La capra bugiarda"
        >
          <figure class="figure figure--goat" />
        </app-text-header>
        <AppParagraph>
          {{ mainData.grikoSummary }}
        </AppParagraph>
      </section>
      <section class="section__text section__text--right">
        <app-text-header
          class="text__header--right"
          content="Il tavolino magico, l'asino d'oro e il randello castigamatti"
        >
          <figure class="figure figure--grimms" />
        </app-text-header>
        <AppParagraph>
          {{ mainData.grimmsSummary }}
        </AppParagraph>
      </section>
    </main>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { mapState } from "vuex";
import AppHeader from "@/components/AppHeader.vue";
import AppTextHeader from "@/components/AppTextHeader.vue";
import AppParagraph from "~/components/AppParagraph.vue";

export default Vue.extend({
  components: {
    AppHeader,
    AppParagraph,
    "app-text-header": AppTextHeader,
  },
  computed: {
    ...mapState(["mainData"]),
  },
});
</script>

<style lang="scss">
.figure {
  &--goat {
    background: url(~/assets/capra.jpg);
    background-size: contain;
    background-position: center;
    height: 4rem;
    width: 4rem;
    border-radius: 1000px;
    margin: 0;
  }

  &--grimms {
    background: url(~/assets/grimms.jpg);
    background-size: contain;
    background-position: center;
    height: 4rem;
    width: 4rem;
    border-radius: 1000px;
    margin: 0;
  }
}

.text__header {
  &--left {
    align-self: flex-start;
    margin-left: 10rem;
    margin-bottom: 5rem;
  }
  &--right {
    align-self: flex-end;
    margin-right: 10rem;
    margin-bottom: 5rem;
  }
}

.section__text {
  margin-top: 8rem;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;

  &--right {
    text-align: right;
  }

  &--left {
    text-align: left;
  }
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
