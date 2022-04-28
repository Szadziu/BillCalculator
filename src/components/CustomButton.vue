<template>
  <button :class="$style.button"><slot></slot></button>
</template>

<script>
export default {
  name: 'custom-button',
};
</script>

<style module>
.button {
  color: white;
  background: hsl(298, 67%, 47%);
  border: none;
  border-radius: 5px;
  padding: 10px 15px;
  margin-left: 10px;
  font-size: 20px;
  cursor: pointer;
  margin-top: 20px;
}
</style>
