<template>
  <div>
    <div id="productForm">
      <label for="productName">Product name:</label>
      <input
        type="text"
        name="productName"
        id="productName"
        v-model="productName"
      />
      <br />
      <label for="productPrice">Product price:</label>
      <input
        type="number"
        name="productPrice"
        id="productPrice"
        v-model="productPrice"
      />
      <br />
      <label for="productQty">Product Quantity:</label>
      <input
        type="number"
        name="productQty"
        id="productQty"
        v-model="productQty"
      />

      <br />
      <label for="productAmount">Product Amount</label>
      <input
        disabled
        type="number"
        name="productAmount"
        id="productAmount"
        v-bind:value="calculateAmount"
      />
      <br />

      <button @click="saveProduct">Save</button>
    </div>

    <div id="showProduct">
      <table border="2">
        <thead>
          <tr>
            <th>ID</th>
            <th>Product Name</th>
            <th>Product Price</th>
            <th>Product Quantity</th>
            <th>Product Amount</th>
          </tr>
        </thead>
        <tbody v-if="productList.length > 0">
          <tr v-for="(product, index) in productList" :key="index">
            <td>{{ index }}</td>
            <td>{{ product.productName }}</td>
            <td>{{ product.productPrice }}</td>
            <td>{{ product.productQty }}</td>
            <td>{{ product.productAmount }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      productName: '',
      productPrice: 0.0,
      productQty: 0,
      productAmount: 0,
      productList: [{}],
    }
  },
  methods: {
    saveProduct() {
      this.productList.push({
        productName: this.productName,
        productPrice: this.productPrice,
        productQty: this.productPrice,
        productAmount: this.productAmount
      });
    },
  },

  computed: {
    calculateAmount() {
      this.productAmount = this.productPrice * this.productQty; 
      return this.productAmount;
    },
  },
}
</script>
