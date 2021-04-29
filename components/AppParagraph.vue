<template>
  <p>
    <slot></slot>
  </p>
</template>

<style lang="scss" scoped>
p {
  font-family: "Raleway";
  font-size: 2.5vmin;
  width: 85%;
}

@media screen and (max-width: 768px) {
  p {
    font-size: 4vmin;
  }
}
</style>
