<template>
  <div id="input-balance-data">
    <table class="input-table">
        <tr class="table-header">
          <th class="unit-price">単価</th>
          <th class="sales-book-sum">売上数</th>
          <th class="sales">売上金額</th>
          <th class="cost-item">品目</th>
          <th class="cost">費用</th>
          <th class="benefit">利益</th>
        </tr>
        <tr class="input-box">
          <td><input type="number" class="unit-price-number" v-model="unitPrice"></td>
          <td><input type="number" class="sales-book-sum-number" v-model="salesBookSum"></td>
          <td><div class="sales-number"></div>{{ calcBookSales }}</td>
          <td><input type="text" class="cost-item-name" v-model="costItemName"></td>
          <td><input type="number" class="cost-number" v-model="cost"></td>
          <td><div class="benefit-number"></div>{{ calcBenefit }}</td>
        </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'InputBalanceData',
  data() {
    return {
      benefit: '',
      costItemName: '',
      salesBookSum: '',
      unitPrice: '',
    };
  },
  computed: {
    calcBookSales() {
      const salesResult = this.unitPrice * this.salesBookSum;
      return salesResult;
    },
  },
  methods: {
      calcBenefit() {
      const benefitResult = this.calcBookSales - this.cost;
      return benefitResult;
    },
  },
};

</script>

<style lang="scss" scoped>
table {
  width: 80vw;
}

td {
  vertical-align: middle;
}
</style>
