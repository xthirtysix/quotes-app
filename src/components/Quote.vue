<template>
  <b-col class="col" cols="12" sm="6" md="4" lg="3">
    <b-card class="quote">
      <slot></slot>
    </b-card>
  </b-col>
</template>

<script>
</script>

<style lang="scss" scoped>
.quote {
  font-family: 'Bad Script', cursive;
  font-size: 2rem;
  color: lightgray;
  cursor: pointer;

  &:hover {
    background-color: var(--red);
    color: var(--white);
  }
}

.col {
  margin-bottom: 2rem;
}
</style>
