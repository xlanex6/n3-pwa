<template>
  <div class="flex justify-between w-full h-12 bg-green-800 text-white ">
    <NuxtLink v-for="{ href, name } in menuItems" :to="href" class="w-1/3 h-full text-center">{{ name }}</NuxtLink>
  </div>
  </template>

<script setup>
const menuItems = [
  { name: 'Home', href: '/' },
  { name: 'Cart', href: '/cart' },
  { name: 'Contact', href: '/contact' },
]
</script>
