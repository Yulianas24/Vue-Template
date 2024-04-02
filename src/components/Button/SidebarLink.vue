<script setup>
defineProps(['to', 'name'])
</script>
<template>
  <router-link
    :class="$route.name == name ? 'bg-gray-600 text-white' : 'bg-gray-300  text-black'"
    class="text-sm py-2 px-5 rounded-lg hover:shadow-md"
    :to="to"
  >
    {{ name }}
  </router-link>
</template>
