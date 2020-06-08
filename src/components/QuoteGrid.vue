<template>
  <b-row>
    <app-quote
      :key="i + Date.now()"
      v-for="(quote, i) in quotes"
      @click.native="deleteQuote(i)">
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
  methods: {
    deleteQuote(i) {
      this.$emit('quoteDeleted', i);
    },
  },
};
</script>

<style>
</style>
