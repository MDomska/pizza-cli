<template>
  <div>
    <div class="product-image" v-bind:style="{ 'background-image': 'url(' + image + ')' }"></div>
    <div class="product-info">
      <h2 class="product-title">{{ title }}</h2>
      <p class="product-description">{{ description }}</p>
      <span class="product-price">{{ price }}</span>
    </div>
  </div>
</template>


<script>
export default {
  props: ["image", "title", "description", "price"]
};
</script>