<template>
  <div class="grid grid-cols-1 w-full gap-4">
    <DishCard v-for="burger in burgers" :key="burger.id" :burger="burger" />
  </div>
</template>

<script setup>
import burgers from '~/data/burgers.json'


</script>
