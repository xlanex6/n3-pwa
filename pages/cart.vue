<template>
  <template v-if="cart?.length > 0">
  
    <div v-for="dish in cart" ::key="dish.id" class="flex items-center justify-between space-x-4 space-y-4 my-2">
      <div class=" items-center flex space-x-4">
        
        <img :src="dish.img" :alt="dish.name" class="w-24 aspect-square" loading="lazy">
        <p>{{ dish.name }}</p>
      </div>
      <div>
        <p>{{ dish.price / 100 }} $</p>
      </div>
      
      
    </div>
  </template>
    <div class="flex justify-center text-xl font-bold">
      TOTAL: {{ cart?.reduce((acc, dish) => acc + dish.price, 0) / 100  || 0}} $
    </div>
    <div class="flex justify-center">
      <button class="bg-red-600 w-[80%] text-white py-2 rounded-full"> VALIDATE</button>
    </div>
</template>

<script setup>
const cart = useState('cart')
</script>
