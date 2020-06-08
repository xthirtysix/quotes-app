<template>
  <b-row class="header">
    <b-col sm="12">
      <h3>Quotes added</h3>
       <b-progress
       :max="maxQuotes">
        <b-progress-bar :value="quoteCount"> {{quoteCount}} / {{maxQuotes}} </b-progress-bar>
       </b-progress>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: [
    'quoteCount',
    'maxQuotes',
  ],
};
</script>

<style>
.header {
  margin-bottom: 2rem;
}
</style>
