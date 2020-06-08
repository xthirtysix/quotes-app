<template>
  <b-form class="row form">
    <b-form-group class="col-sm-12" label="Quote:" label-for="quote">
      <b-form-textarea
      rows="3"
      v-model="quote"
      id="quote">
      </b-form-textarea>
    </b-form-group>
    <b-button
    class="mx-auto"
    type="submit"
    variant="primary"
    @click.prevent="createNew">
      Add quote
    </b-button>
  </b-form>
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

<style scoped>
.form {
  margin-bottom: 2rem;
}
</style>
