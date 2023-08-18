<template>
    <div class="container mt-3">
    <h1>Product List</h1>
    <div class="row justify-content center nt-3">
      <div class="col-md-12">
        <table class="table">
      <thead>
        <tr>
          <th>Name</th>
          <th>Price</th>
          <th>Description</th>
          <th>ID</th>
          <th>Date</th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(product, index) in products" :key="index">
          <td>{{ product.prod_name }}</td>
          <td>{{ product.prod_price }}</td>
          <td>{{ product.prod_desc }}</td>
          <td>{{ product.prod_id }}</td>
          <td>{{ product.prod_date }}</td>
          <td>
            <button @click="editProduct(index)" class="btn btn-primary btn-sm">Edit</button>
            <button @click="deleteProduct(index)" class="btn btn-danger btn-sm">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>
      </div>
    </div>
  </div>
  </template>
  
  <script>
  export default {
  name: "detailProduct",
  data() {
    return {
      products: []
    };
  },
  mounted() {
    this.fetchProducts();
  },
  methods: {
    fetchProducts() {
      const products = JSON.parse(localStorage.getItem('products')) || [];
      this.products = products;
    },
    deleteProduct(index) {
      this.products.splice(index, 1);
      localStorage.setItem('products', JSON.stringify(this.products));
    },editProduct(index) {
      this.$router.push({ name: 'edit-product', params: { index } });
    }
  }
};
  
  </script>
  
  <style scoped>
  
  </style>