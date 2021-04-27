<template>
  <section
    class="masthead"
    role="img"
    aria-label="Image Description"
  >
    <h1>
      <span class="head--1">
        La
      </span>
      <span class="head--2">
        Grecìa
      </span>
      <span class="head--3">
        Salentina
      </span>
    </h1>
    <a href="#page-start"><img src="~/assets/down.svg" class="down"></a>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.down {
  z-index: 1000;
  position: absolute;
  transform: translate(-50%, -50%);
  top: 80%;
  left: 50%;
  display: none;
}

.masthead {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
  width: 100%;
  height: 95vh; /* if you don't want it to take up the full screen, reduce this number */
  overflow: hidden;
  background-size: cover !important;
  background: linear-gradient(
      to right bottom,
      rgba(#11698e, 0.85),
      rgba(#16c79a, 0.85)
    ),
    url("~/assets/hero.jpg") no-repeat center center scroll;
}

h1 {
  font-style: normal;
  font-family: "Poppins";
  color: #eee;
  font-size: 9vmin;
  letter-spacing: 0.03em;
  font-weight: 100;
  line-height: 1;
  margin-bottom: 2vh;

  & span {
    display: block;
  }
  & .head--1 {
    font-size: 10vmin;
  }
  & .head--2 {
    font-weight: 100;
    font-size: 20vmin;
  }
  & .head--3 {
    font-size: 12vmin;
  }
}

button {
  background: #098191;
  transition: background ease 0.25s;
  border-radius: 42px;
  display: inline-block;
  border: none;
  padding: 0.75rem 1.5rem;
  margin: 0;
  text-decoration: none;
  color: #ffffff;
  font-size: 1.2rem;
  cursor: pointer;
  text-align: center;
  -webkit-appearance: none;
  -moz-appearance: none;
}
button:hover {
  background: #63b6b8;
}
button:focus {
  outline: 1px solid #fff;
  outline-offset: -4px;
}

@media screen and (max-width: 480px) {
  .masthead {
    height: 100vh;
  }

  .down {
    display: block;
  }
}
</style>
