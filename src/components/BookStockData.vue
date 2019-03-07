<template>
  <div id="book-stock-data">
    <table class="input-table">
        <tr class="table-header">
          <th class="book-name">タイトル</th>
          <th class="order">注文数</th>
          <th class="deliverly-books">納入冊数</th>
          <th class="free-distribution">無料配付</th>
          <th class="book-stock">在庫</th>
          <th class="sales-book-">頒布数</th>
        </tr>
        <tr class="input-box">
          <td><input type="text" class="book-name-text" v-model="bookName"></td>
          <td><input type="number" class="order-" v-model="order"></td>
          <td><input type="number" class="deliverly-books-" v-model="deliverBooks"></td>
          <td><input type="number" class="free-distribution-" v-model="freeDistribution"></td>
          <td><input type="number" class="book-stock-number" v-model="bookStock"></td>
          <td><p class="sales-book-result"> {{ salesBook }} </p></td>
        </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'BookStockData',
  data() {
    return {
      bookName: '',
      order: '',
      deliverBooks: '',
      freeDistribution: '',
      bookStock: '',
    };
  },
  computed: {
    salesBook() {
      const sales = (this.deliverBooks - this.freeDistribution) - this.bookStock;
      return sales;
    },
  },
};
</script>

<style lang="scss" scoped>
table {
  align-items: center;
  width: 80vw;
}
</style>
