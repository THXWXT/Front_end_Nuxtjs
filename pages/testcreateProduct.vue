<template>
    <div class="container mt-3">
      <h1>Add Product</h1>
      <form @submit.prevent="saveProduct">
        <div class="input-group mb-3">
            <span class="input-group-text" id="basic-addon1">Name Product</span>
            <input type="text" v-model="product.prod_name" class="form-control" aria-label="Username"
              aria-describedby="basic-addon1">
          </div>
          <div class="input-group mb-3">
            <span class="input-group-text" id="basic-addon1">Price Product</span>
            <input type="text" v-model="product.prod_price" class="form-control" aria-label="Username"
              aria-describedby="basic-addon1">
          </div>
          <div class="input-group mb-3">
            <span class="input-group-text" id="basic-addon1">Product Desc</span>
            <input type="text" v-model="product.prod_desc" class="form-control" aria-label="Username"
              aria-describedby="basic-addon1">
          </div>
          <div class="input-group mb-3">
            <span class="input-group-text" id="basic-addon1">ID</span>
            <input type="text" v-model="product.prod_id" class="form-control" aria-label="Username"
              aria-describedby="basic-addon1">
          </div>
          <div class="input-group mb-3">
            <span class="input-group-text" id="basic-addon1">Time</span>
            <input type="date" v-model="product.prod_date" class="form-control" aria-label="Username"
              aria-describedby="basic-addon1">
          </div>
          
        <div class="form-group">
          <button class="btn btn-primary btn-block" type="submit">Add Product</button>
        </div>
      </form>
    </div>
  </template>
  
  <script>
  
  </script>
  