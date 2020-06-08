<template>
  <b-container id="app">
    <app-header :maxQuotes="maxQuotes" :quoteCount="quotes.length"/>
    <app-new-quote @quoteAdded="newQuote"/>
    <b-row>
      <b-col sm="12">
        <b-alert>Info: Click on a Quote to delete it.</b-alert>
      </b-col>
    </b-row>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"/>
  </b-container>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
import Header from './components/Header.vue';

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
    appHeader: Header,
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('Please delete quote first');
      }

      return this.quotes.push(quote);
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
