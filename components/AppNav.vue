<template>
  <div class="container-fluid nav__parent">
    <div class="nav__container">
      <nav class="navbar navbar-expand " :class="`navbar-${mode}`">
        <div class="container-fluid">
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
            aria-controls="navbarNav"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon" />
          </button>
          <div
            id="navbarNav"
            class="collapse navbar-collapse"
          >
            <ul class="navbar-nav">
              <li class="nav-item">
                <nuxt-link
                  to="/"
                  class="nav-link"
                  href="#"
                >
                  Home
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link
                  to="/griko"
                  class="nav-link"
                  href="#"
                >
                  Griko
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link
                  to="/history"
                  class="nav-link"
                  href="#"
                >
                  Storia
                </nuxt-link>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    mode: {
      type: String,
      default: 'dark'
    }
  }
}
</script>

<style lang="scss" scoped>
.nav__container {
  width: 15rem;
  font-size: 1.1rem;
}

.nav__parent {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: transparent;
}

// @media screen and (max-width: 992px) {
//   .nav__container {
//     width: 100%;
//   }

//   .nav__parent {
//     display: flex;
//     align-items: center;
//     justify-content: flex-start;
//   }
// }

</style>
