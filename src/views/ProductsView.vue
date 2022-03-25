<template>
  <div class="about">
    <main class="wrapper">
      <h1>Products</h1>

      <div class="card-container">
        <ProductCard
          v-for="(product, index) in inventory.slice(0,9)"
          :key="product.id"
          :product="product"
          :addToCart="addToCart"
          :index="index"
        />
      </div>
    </main>
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'

export default {
  name: 'ProductView',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
