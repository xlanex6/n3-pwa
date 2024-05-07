<template>
  <div class="h-12 flex justify-end px-4 bg-green-800 items-center text-white">
    <div>CART <span v-show="cart?.length > 0">( {{ cart?.length }} )</span> </div>
  </div>
</template>

<script setup>
const cart = useState('cart')
</script>
