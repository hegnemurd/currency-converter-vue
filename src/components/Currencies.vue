<template>
  <div id="app">
      <span>Amount: </span>
      <input
        class="input"
        id="pounds"
        v-model.number="amount"
        type="number"
        placeholder="Enter Amount"
      />
      <br />
      <span>Convert From: </span>
      <select v-model="convertFrom" style="width: 100px">
        <option
          v-for="(cur, index) in currencyFrom"
          :key="(cur, index)"
          v-bind:value="cur.name"
        >
          {{ cur.fulln }}
        </option>
      </select>
      <span>Convert To: </span>
      <select v-model="convertTo" style="width: 100px">
        <option
          v-for="(cur, index) in currencyFrom"
          :key="(cur, index)"
          v-bind:value="cur.name"
          >{{ cur.fulln }}</option
        >
      </select>
      <br />
      <span
        >{{ amount }} {{ convertFrom }} is equal to {{ finalAmount }}
        {{ convertTo }}</span
      >
  </div>
</template>
<!-- 
     1)App will convert between different units and show the result.
     2)Currencies Supported: GBP, EUR, USD, AUD, CAD
     3)Digital Storage Supported: GB, MB, KB, TB
     4)- UI (User Interface, what it looks like) will look 
     similar to the unit converter from Google.
     6)Have a "fixed" position footer at the bottom of the browser viewport.
     7)Footer will display the result of the conversion.    
     8)Use Vuex store, you will need state, mutations and getters (no actions yet).
     9)Could do it with Math() and with whatever the currency is, either 
     divide or multiply with a certain number... instead of using the code
     that w3schools use.
-->
<script>

// new Vue({
//   el: "#app",
//   data: {
//     name: "",
//     currencyFrom: [
//       { name: "GBP", fulln: "British Pound" },
//       { name: "EUR", fulln: "Euro" },
//       { name: "USD", fulln: "American Dollar" },
//       { name: "AUD", fulln: "Australian Dollar" },
//       { name: "CAD", fulln: "Canadian Dollar" }
//     ],
//     convertFrom: "GBP",
//     convertTo: "EUR",
//     amount: ""
//   },
//   computed: {
//     finalAmount: function() {
//       var to = this.convertTo;
//       var from = this.convertFrom;
//       var final;
//       switch (from) {
//         case "GBP":
//           if (to == "EUR") {
//             final = this.amount * 1.2;
//           }
//           if (to == "USD") {
//             final = this.amount * 1.29;
//           }
//           if (to == "AUD") {
//             final = this.amount * 1.96;
//           }
//           if (to == "CAD") {
//             final = this.amount * 1.71;
//           }
//           break;
//         case "EUR":
//           if (to == "GBP") {
//             final = this.amount * 0.84;
//           }
//           if (to == "USD") {
//             final = this.amount * 1.08;
//           }
//           if (to == "AUD") {
//             final = this.amount * 1.64;
//           }
//           if (to == "CAD") {
//             final = this.amount * 1.43;
//           }
//           break;
//         case "USD":
//           if (to == "GBP") {
//             final = this.amount * 0.77;
//           }
//           if (to == "EUR") {
//             final = this.amount * 0.93;
//           }
//           if (to == "AUD") {
//             final = this.amount * 1.52;
//           }
//           if (to == "CAD") {
//             final = this.amount * 1.33;
//           }
//           break;
//         case "AUD":
//           if (to == "GBP") {
//             final = this.amount * 0.51;
//           }
//           if (to == "EUR") {
//             final = this.amount * 0.61;
//           }
//           if (to == "USD") {
//             final = this.amount * 0.66;
//           }
//           if (to == "CAD") {
//             final = this.amount * 0.87;
//           }
//           break;
//         case "CAD":
//           if (to == "GBP") {
//             final = this.amount * 0.58;
//           }
//           if (to == "EUR") {
//             final = this.amount * 0.7;
//           }
//           if (to == "USD") {
//             final = this.amount * 0.75;
//           }
//           if (to == "AUD") {
//             final = this.amount * 1.14;
//           }
//           break;
//       }
//       return final;
//     }
//   }
// });

export default {
 data() {
   return {
     pounds: null,
     euros: null
   };
 },
 methods: {
   calculateGbpToEur() {
     const pounds = pounds;
     const euros = euros;
     const calculatedEuros = Math.round(Math.imul(pounds, euros));
     console.log(Math.imul(pounds, 1.2));
     return calculatedEuros;
   }
 }
};
</script>

<style></style>
