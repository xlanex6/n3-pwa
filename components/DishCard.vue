<template>
  <div class="m-auto">
    <img :src="burger.img" :alt="burger.name" class="w-64 aspect-square" loading="lazy">
    <div class="flex justify-between">
      <h3>{{ burger.name }}</h3>
      <p>{{ burger.price / 100 }} $</p>
    </div>
    <button class="w-full text-white uppercase font-semi bg-red-600 rounded-full py-1 "
      @click="addToCart">Ajouter</button>

  </div>
</template>

<script setup>
const props = defineProps(['burger'])

const cart = useState('cart', () => [])

function addToCart() {
  cart.value.push(props.burger)
}

</script>
