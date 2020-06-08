<template>
  <b-row>
    <b-col>
      <b-form>
        <b-form-group label="Quote:" label-for="quote">
          <b-form-textarea
          rows="3"
          v-model="quote"
          id="quote">
          </b-form-textarea>
        </b-form-group>
        <b-button
        type="submit"
        variant="primary"
        @click.prevent="createNew">
          Add quote
        </b-button>
      </b-form>
    </b-col>
  </b-row>
</template>

<script>
export default {
  data() {
    return {
      quote: '',
    };
  },
  methods: {
    createNew() {
      this.$emit('quoteAdded', this.quote);
      this.quote = '';
    },
  },
};
</script>

<style>
</style>
