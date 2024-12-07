<script>
import products from '~/static/products.json';
import ProductCard from '../components/ProductCard.vue';
import LanguageSwitcher from '../components/LanguageSwitcher.vue';

export default {
  components: { ProductCard, LanguageSwitcher },
  data() {
    return {
      items: products
    };
  }
};
</script>

<template>
  <div>
    <LanguageSwitcher />
    <h1>{{ $t('welcome') }}</h1>
    <div class="product-list">
      <ProductCard :title="$t('product_a')" :price="$t('product_a_price')"/>
      <ProductCard :title="$t('product_b')" :price="$t('product_b_price')"/>
      <ProductCard :title="$t('product_c')" :price="$t('product_c_price')"/>
    </div>
  </div>
</template>

<style scoped>
.product-list {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}
</style>







