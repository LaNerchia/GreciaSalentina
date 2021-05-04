<template>
  <main class="main">
    <AppNav mode="light" />
    <section
      id="page-start"
      class="section__text section__text--left"
    >
      <a
        class="text__header--left"
        href="https://www.ciuricepedi.it/fiaba-16-e-guscia-fsematara/"
      >
        <app-text-header content="E guscia fsematara">
          <figure class="figure figure--goat" />
        </app-text-header>
      </a>
      <AppParagraph>
        {{ mainData.grikoSummary }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--right">
      <a
        class="text__header--right"
        href="https://www.grimmstories.com/it/grimm_fiabe/il_tavolino_magico_asino_oro_e_randello_castigamatti"
      >
        <app-text-header content="Il tavolino magico, l'asino d'oro e il randello castigamatti">
          <figure class="figure figure--grimms" />
        </app-text-header>
      </a>
      <AppParagraph>
        {{ mainData.grimmsSummary }}
      </AppParagraph>
    </section>
    <section class="section__text section__text--center">
      <app-text-header
        class="text__header--center"
        content="Differenze"
      />
      <AppParagraph>
        {{ mainData.differences }}
      </AppParagraph>
      <div class="container">
        <table class="table">
          <thead>
            <tr>
              <th scope="col">
                Caratteristiche
              </th>
              <th scope="col">
                Il il tavolino magico asino oro e randello castigamatti
              </th>
              <th scope="col">
                E guscia fsematara
              </th>
              <th scope="col">
                Riflessioni
              </th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">
                Personaggi
              </th>
              <td>/</td>
              <td>/</td>
              <td>
                sono uguali in entrambi solo che in quella dei grimm interviene il locandiere
              </td>
            </tr>
            <tr>
              <th scope="row">
                Tempo
              </th>
              <td>
                i fatti si svolgono in un tempo più lungo
              </td>
              <td>
                i fatti si svolgono in un tempo più corto
              </td>
              <td>/</td>
            </tr>
            <tr>
              <th scope="row">
                Spazio
              </th>
              <td>
                aperto alternato con chiusi
              </td>
              <td>
                aperto alternato a chiusi
              </td>
              <td>/</td>
            </tr>
            <tr>
              <th scope="row">
                Elementi magici
              </th>
              <td>
                si
              </td>
              <td>
                no
              </td>
              <td>/</td>
            </tr>
            <tr>
              <th scope="row">
                Funzioni di propp
              </th>
              <td>
                allontanamento/partenza/ritorno
              </td>
              <td>
                no
              </td>
              <td>
                nella seconda non c'è un vero e proprio allontamento in quanto i figli muoiono
              </td>
            </tr>
          </tbody>
        </table>
      </div>
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
    ...mapState(['mainData'])
  }
})
</script>

<style lang="scss" scoped>
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
    animation-name: moveInBottom;
    animation-duration: 1s;
  }
}

.container-normal {
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
