<template>
  <b-row class="row">
    <app-quote
      :key="quote + Date.now()"
      v-for="quote in quotes">
      {{ quote }}
    </app-quote>
  </b-row>
</template>

<script>
import Quote from './Quote.vue';

export default {
  props: ['quotes'],
  components: {
    appQuote: Quote,
  },
};
</script>

<style>
.row {
  font-family: 'Bad Script', cursive;
  font-size: 2rem;
  color: lightgray;
}
</style>
