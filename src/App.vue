<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css?family=M+PLUS+Rounded+1c" rel="stylesheet">
    <app-header></app-header>
    <div class="book-stock-data">
      <book-stock-data></book-stock-data>
    </div>
    <div class="balance-data">
      <input-balance-data></input-balance-data>
    </div>
  </div>
</template>

<script>
import 'normalize.css'
import AppHeader from './components/AppHeader.vue'
import BookStockData from './components/BookStockData.vue'
import InputBalanceData from './components/InputBalanceData.vue'

export default {
  name: 'app',
  components: {
    'app-header': AppHeader,
    'book-stock-data': BookStockData,
    'input-balance-data': InputBalanceData,
  },
};
</script>

<style lang="scss">
#app {
  font-family: "M PLUS Rounded 1c";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.main-contents {
  align-items: center;
  display: flex;
}
</style>
