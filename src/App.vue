<script setup lang="ts">
import TheHeader from './components/Header.vue'
import TheFooter from './components/Footer.vue'
import Cart from './components/Cart/Cart.vue'
import Shop from './components/Shop/Shop.vue'
import data from './data/product';
import { reactive } from 'vue';
import type { ProductInterface } from './interfaces/product.interface';

const products = reactive<ProductInterface[]>(data)
</script>

<template>
  <div class="app-container">
    <TheHeader class="header"/>
    <Shop :products="products" class="shop"/>
    <Cart class="cart"/>
    <TheFooter class="footer"/>
  </div>
</template>

<style lang="scss">
@import './assets/base.scss';
@import './assets/debug.scss';

.app-container {
  min-height: 100vh;
  display: grid;
  grid-template-areas: "header header" "shop cart" "footer footer";
  grid-template-columns: 75% 25% ;
  grid-template-rows: 48px auto 48px;
}

.header {
  grid-area: header;
}

.shop {
  grid-area: shop;
}

.cart {
  grid-area: cart;
  border-left: var(--border);
  background-color: white;
}

.footer {
  grid-area: footer;
}
</style>
