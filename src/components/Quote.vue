<template>
  <b-col col sm="6" md="4" lg="3">
    <b-card class="quote">
      <slot></slot>
    </b-card>
  </b-col>
</template>

<script>
</script>

<style lang="scss">
.quote {
  cursor: pointer;

  &:hover {
    background-color: var(--red);
    color: var(--white);
  }
}
</style>
