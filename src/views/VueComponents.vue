<script setup>
import { ref } from 'vue'
import TabNavigation from '../components/Tab/TabNavigation.vue'

const active_tab = ref('tab-1')
const tab_list = ref(['tab-1', 'tab-2'])
</script>

<template>
  <div class="flex flex-col h-full">
    <p class="mb-3">Vue Components</p>
    <!-- navigation -->
    <TabNavigation :tab-list="tab_list" v-model="active_tab" />
    <!-- content -->
    <div class="p-5 w-full h-full bg-gray-300 rounded-b-xl rounded-tr-xl"></div>
  </div>
</template>
