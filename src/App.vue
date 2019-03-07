<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css?family=M+PLUS+Rounded+1c" rel="stylesheet">
    <app-header></app-header>
    <div class="book-stock-data">
      <add-book-stock-line></add-book-stock-line>
      <book-stock-data></book-stock-data>
    </div>
    <div class="balance-data">
      <add-table-line></add-table-line>
      <input-balance-data></input-balance-data>
    </div>
    <csv-download></csv-download>
  </div>
</template>

<script>
import 'normalize.css'
import AppHeader from './components/AppHeader.vue'
import AddTableLine from './components/AddTableLine.vue'
import AddBookStockLine from './components/AddBookStockLine.vue'
import BookStockData from './components/BookStockData.vue'
import CsvDownload from './components/CsvDownload.vue'
import InputBalanceData from './components/InputBalanceData.vue'

export default {
  name: 'app',
  components: {
    'add-book-stock-line': AddBookStockLine,
    'app-header': AppHeader,
    'add-table-line': AddTableLine,
    'book-stock-data': BookStockData,
    'csv-download': CsvDownload,
    'input-balance-data': InputBalanceData
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
