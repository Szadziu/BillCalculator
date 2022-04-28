<template>
  <div id="app">
    <BillInput :value="billValue" @onChange="handleBillInput" />
    <ServiceRating />
    <CustomButton>Oblicz</CustomButton>
    <InfoModal />
  </div>
</template>

<script>
import BillInput from '@/components/BillInput.vue';
import ServiceRating from '@/components/ServiceRating.vue';
import CustomButton from '@/components/CustomButton.vue';
import InfoModal from '@/components/InfoModal.vue';

export default {
  name: 'App',
  components: {
    BillInput,
    ServiceRating,
    CustomButton,
    InfoModal,
  },
  data: function () {
    return { billValue: 25 };
  },
  methods: {
    handleBillInput(value) {
      this.billValue = value;
    },
  },
};
</script>

<style module>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
