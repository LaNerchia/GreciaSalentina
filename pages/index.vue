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
      Realizzato con VUE3, Nuxt, Netlify e un pizzico di bootstrap
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
