<script setup>
defineProps(['tabList'])
const active = defineModel()
</script>
<template>
  <div class="flex w-fit rounded-t-lg overflow-hidden">
    <button
      v-for="menu in tabList"
      :key="menu"
      class="px-10 pt-2 pb-4 text-sm"
      @click="active = menu"
      :class="active.name == menu.name ? 'bg-gray-300' : 'bg-gray-600 text-white'"
    >
      {{ menu.name }}
    </button>
  </div>
</template>
