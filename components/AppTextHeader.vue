<template>
  <div class="body">
    <div class="content">
      <h3>
        {{ content }}
      </h3>
      <slot></slot>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    content: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="scss" scoped>
.body {
  display: block;
  padding: 2rem 4rem;
  background: linear-gradient(
    to right bottom,
    rgba(#11698e, 1),
    rgba(#16c79a, 1)
  );
  transform: skewX(-16deg);
}

.content {
  display: flex;
  align-items: center;
  justify-content: center;
  transform: skewX(16deg);

  & h3 {
    font-weight: 200;
    font-family: 'Poppins';
    color: #fff;
    margin: .5rem;
    margin-right: 2rem;
  }
}

@media screen and (max-width: 768px) {
  .body {
    width: 100vw;
    transform: skewX(0);
  }

  .content {
    transform: skewX(0);
    & h3 {
      margin: 0;
    }
  }
}
</style>
