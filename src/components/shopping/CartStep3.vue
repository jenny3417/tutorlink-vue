<template>
    <navbar></navbar>
    <div class="contailer-lg">
        <n-result status="success" title="已成功下單" description="請於下單後3小時內付款">
            <button class="btn btn-outline-success" type="button">
                <router-link to="/" class="rlink">回首頁</router-link>
            </button>
        </n-result>
    </div>
</template>
      
<script setup>
import Navbar from "@/components/public/Navbar.vue"
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