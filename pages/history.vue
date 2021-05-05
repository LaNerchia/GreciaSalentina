<template>
  <main class="history-section">
    <AppNav mode="light" />
    <section class="section__text section__text--left">
      <app-text-header
        content="Introduzione"
        class="text__header--left"
      />
      <AppParagraph>
        {{ historyData.introduction }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--right">
      <app-text-header
        content="Come ebbe inizio?"
        class="text__header--right"
      />
      <AppParagraph>
        {{ historyData.start }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--left">
      <app-text-header
        content="Religione"
        class="text__header--left"
      />
      <AppParagraph>
        {{ historyData.religion }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--right">
      <app-text-header
        content="Cosa succede dopo?"
        class="text__header--right"
      />
      <AppParagraph>
        {{ historyData.history }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--left">
      <app-text-header
        content="Come nasce la grecia salentina?"
        class="text__header--left"
      />
      <AppParagraph>
        {{ historyData.born }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--center">
      <app-text-header
        content="Il portale del griko"
        class="text__header--center"
      />
      <AppParagraph>
        {{ salvatoreTommasi.ciuriCePedi }}
      </AppParagraph>
      <ul class="list-group">
        <li
          v-for="p in salvatoreTommasi.ciuriCePediList"
          :key="p"
          class="list-group-item px-5"
        >
          {{ p }}
        </li>
      </ul>
    </section>
    <section class="section__text section__text--left">
      <app-text-header
        content="Il manuale per ragazzi"
        class="text__header--left"
      />
      <AppParagraph>
        {{ salvatoreTommasi.manual }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--right">
      <app-text-header
        content="Salvatore Tommasi"
        class="text__header--right"
      />
      <AppParagraph>
        {{ salvatoreTommasi.life }}
      </AppParagraph>
    </section>
  </main>
</template>

<script>
import Vue from 'vue'
import { mapState } from 'vuex'
import AppTextHeader from '@/components/AppTextHeader.vue'
import AppParagraph from '~/components/AppParagraph.vue'

export default Vue.extend({
  components: {
    AppParagraph,
    'app-text-header': AppTextHeader
  },
  computed: {
    ...mapState([
      'historyData'
    ]),
    ...mapState([
      'salvatoreTommasi'
    ])
  }
})
</script>

<style lang="scss" scoped>
.history-section {
  margin: 0 10rem;
  display: flex;
  flex-direction: column;
}

.text__header {
  &--left {
    &:link,
    &:active {
      text-decoration: none;
    }
    text-decoration: none;
    align-self: flex-start;
    margin-left: 10rem;
    margin-bottom: 5rem;
  }
  &--right {
    &:link,
    &:active {
      text-decoration: none;
    }
    align-self: flex-end;
    margin-right: 10rem;
    margin-bottom: 5rem;
  }
  &--center {
    &:link,
    &:active {
      text-decoration: none;
    }
    text-decoration: none;
    align-self: center;
    margin-top: 10rem;
    margin-bottom: 5rem;
    padding: 2rem 7rem;
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
    animation-name: moveInRight;
    animation-duration: 1s;
  }

  &--left {
    text-align: left;
    animation-name: moveInLeft;
    animation-duration: 1s;
  }
  &--center {
    text-align: center;
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

@media screen and (max-width: 768px) {
  .history-section {
    margin: 0;
  }

  .text__header {
    &--left {
      align-self: center;
      margin-left: 0rem;
    }
    &--right {
      align-self: center;
      margin-right: 0rem;
    }
  }

  .figure {
    &--grimms {
      display: none;
    }
    &--goat {
      display: none;
    }
  }
  .section__text {
    font-size: 0.7rem;

    &--right {
      text-align: center;
    }

    &--left {
      text-align: center;
    }

    margin-top: 2rem;
  }
}
</style>
