<template>
  <div class="mainPage">
    <AppNav
      mode="dark"
      class="main__nav"
    />
    <AppHeader />
    <AppParagraph id="page-start" class="main__paragraph">
      Lavoro realizzato da un gruppo di studenti della IBE
      <br>
      Seguito dalla professoressa Nadia Amico
      <br>
      Realizzato con VUE3, Nuxt, Netlify e un pizzico di bootstrap
      <br>
      <a class="repo" href="https://github.com/LaNerchia/GreciaSalentina">GitHub Repository</a>
    </AppParagraph>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import AppHeader from '@/components/AppHeader.vue'
import AppParagraph from '@/components/AppParagraph.vue'

export default Vue.extend({
  components: {
    AppHeader,
    AppParagraph
  }
})
</script>

<style lang="scss" scoped>
.repo {
  &:link, &:visited {
    text-decoration: none;
    color: #4a47a3;
    font-size: 1.6rem;
    font-family: 'Poppins';
    font-weight: 400;
  }
}

.mainPage {
  flex-direction: column;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}

.main__paragraph {
  margin-top: 4rem;
}

.main__nav {
  margin-bottom: -4rem;
}

// @media screen and (max-width: 992px) {
//   .main__nav {
//     margin-bottom: 0;
//   }
// }
</style>
