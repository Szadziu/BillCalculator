<template>
  <div>
    <p>Wysokość rachunku:</p>
    <label for="billAmount">$ </label>
    <input
      name="billAmount"
      id="billAmount"
      type="number"
      :value="value"
      @input="handleInput"
    />
  </div>
</template>

<script>
export default {
  name: 'bill-input',
  props: ['value'],
  methods: {
    handleInput({ target: { value } }) {
      this.$emit('onChange', value);
    },
  },
};
</script>
