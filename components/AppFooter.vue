<template>
  <div class="footer">
    <h3>Creato da</h3>
    <ul class="footer__list">
      <li>Alessandro Liguori</li>
      <li>Daniele Fersini</li>
      <li>Francesco Cozza</li>
      <li>Gioele Elia</li>
      <li>Giuseppe Spennato</li>
      <li>Simone Depascali</li>
    </ul>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}

.footer {
  margin-top: 5rem;
  background-color: #393e46;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
  align-items: center;
  color: #fff;
  padding: 2rem 0;

  &__list {
    margin-top: 1.5rem;
    display: flex;
    flex-direction: row;
  }
}

li {
  display: inline-block;
  padding: 0 .7rem;
  &:not(:last-child) {
    border-right: 1px solid #fff;
  }
}

@media screen and (max-width: 768px) {
  .footer {
    &__list {
      display: flex;
      flex-direction: column;
    }
  }

  li {
    &:not(:last-child) {
      border: none;
    }
  }
}
</style>
