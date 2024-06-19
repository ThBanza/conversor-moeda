<template>
  <div>
    <input type="text" v-model="realValue">
    <button @click="convertToDollar">Convert</button>
    <h2> BRL:{{ realValue }} para USD:{{ dollarValue }} </h2>
    <h2>{{ dollarValue_value }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      realValue: 0,
      dollarValue: 0,
      exchangeRate: 0.20 // 1 real = 0.20 dollars (example rate)
    }
  },
  methods: {
    convertToDollar() {
      this.dollarValue = this.realValue * this.exchangeRate;
    }
  }
}
</script>
<style scoped>
</style>