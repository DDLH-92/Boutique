<script setup lang="ts"></script>

<template>
  <div class="mb-10 p-10 d-flex flex-row align-items-center product">
    <strong class="flex-fill">Macbook Pro</strong>
    <span class="mr-10">x 1</span>
    <span class="mr-10">Prix: 1500 $</span>
    <button class="btn btn-danger">supprimer</button>
  </div>
</template>

<style lang="scss" scoped>
.product {
  border: var(--border);
  border-radius: var(--border-radius);
  background-color: var(--gray-1);
}
</style>
