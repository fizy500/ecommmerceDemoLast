<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    price: {
      type: Number,
      required: true
    }
  }
};
</script>

<template>
  <div class="product-card">
    <h3>{{ $t('product_title') }}: {{ title}}</h3>
    <p>{{ $t('product_price') }}: {{ price }}</p>
    <button class="product-button">{{ $t('add_to_cart') }}</button>
  </div>
</template>


<style scoped>
.product-card {
  border: 1px solid #ddd;
  background-color: bisque;
  padding: 16px;
  margin: 8px;
  border-radius: 8px;
  text-align: center;
}

.product-button {
  border: 1px solid blueviolet;
  border-radius: 8px;
  padding:5px;
}
</style>