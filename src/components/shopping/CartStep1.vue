<template>
  <navbar></navbar>
  <div class="contailer-lg">
    <div class="card px-0">
      <div class="cart-list-header">
        <div class="row px-0 mx-0">
          <div class="col-10 col-lg-6 mx-0">課程資訊</div>
          <div class="col-2 p-0 d-none d-lg-flex justify-content-center">課程類型</div>
          <div class="col-2 p-0 d-none d-lg-flex justify-content-center">數量</div>
          <div class="col-1 p-0 d-none d-lg-flex justify-content-center">小計</div>
          <div class="col-1 p-0 d-none d-lg-flex"></div>
        </div>
      </div>
      <shopping-cart-item></shopping-cart-item>
      <shopping-cart-item></shopping-cart-item>
      <shopping-cart-item></shopping-cart-item>
      <div class="row px-0 mx-0  pe-2">
        <h5 class="col-6 col-lg-6 mx-0 text-lg-center">總金額</h5>
        <h5 class="col-6 col-lg-6 mx-0 text-lg-center">
          $<n-number-animation ref="numberAnimationInstRef" :from="0" :to="12039" />
        </h5>
      </div>
    </div>
    <button type="button" class="btn btn-outline-success">
      <router-link to="/member/shoppingcart/step2" class="rlink">結帳</router-link>
    </button>
  </div>
</template>
    
<script setup>
import ShoppingCartItem from "@/components/shopping/ShoppingCartItem.vue"
import Navbar from "@/components/public/Navbar.vue"
import { ref } from "vue";
</script>
    

<style scoped>
.cart-list-header {
  font-size: 1.125rem;
  padding: 0.3rem 0;
  background-color: beige;
  border-color: aliceblue;
}

.card {
  width: 85%;
  margin: 15px auto;
}

.btn-outline-success {
  margin: 15px auto;
  display: flex;
  justify-content: center;
}

.rlink {
  color: #198754;
}

.rlink:hover {
  color: aliceblue;
}
</style>