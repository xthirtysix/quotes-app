<template>
  <b-container id="app">
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"/>
    <app-new-quote @quoteAdded="newQuote"/>
    <b-row>
      <b-col sm="12">
        <b-alert>Info: Click on a Quote to delete it.</b-alert>
      </b-col>
    </b-row>
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
    deleteQuote(index) {
      this.quotes.splice(index, 1);
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
