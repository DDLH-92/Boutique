<script setup lang="ts">
import ShopProductList from './ShopProductList.vue'

defineProps<{
  products: ProductInterface[]
}>()

</script>

<template>
  <div>
    <ShopProductList :products="products" />
  </div>
</template>

<style lang="scss" scoped></style>
