<template>
  <div id="app">
    <currency-converter></currency-converter>
    <digital-storage-converter></digital-storage-converter>
  </div>
</template>
<!-- 
     1)App will convert between different units and show the result.
     2)Types of conversions will be: Currency and Digital Storage.
     3)Currencies Supported: GBP, EUR, USD, AUD, CAD
     4)Digital Storage Supported: GB, MB, KB, TB
     5)- UI (User Interface, what it looks like) will look 
     similar to the unit converter from Google.
     6)Have a "fixed" position footer at the bottom of the browser viewport.
     7)Footer will display the result of the conversion.
     8)Use Vuex store, you will need state, mutations and getters (no actions yet).

-->
<script>
import Currencies from "./components/Currencies.vue";
import DigitalStorage from "./components/DigitalStorage.vue";

export default {
  components: {
    "currency-converter": Currencies,
    "digital-storage-converter": DigitalStorage
  }
};
</script>

<style></style>
