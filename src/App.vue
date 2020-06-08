<template>
  <b-container id="app">

    <app-quote-grid :quotes="quotes" />
  </b-container>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';

export default {
  data() {
    return {
      quotes: [
        'Just a quote',
      ],
      maxQuotes: 10,
    };
  },
  components: {
    appQuoteGrid: QuoteGrid,
  },
};
</script>

<style lang="scss">
#app {
  margin-top: 3rem;
}
</style>
