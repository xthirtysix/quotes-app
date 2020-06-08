<template>
  <b-container id="app">
    <app-quote-grid :quotes="quotes" />
    <app-new-quote @quoteAdded="newQuote"/>
  </b-container>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';

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
    appNewQuote: NewQuote,
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
  },
};
</script>

<style lang="scss">
#app {
  margin-top: 3rem;
  font-family: Arial;
}
</style>
