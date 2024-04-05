<script setup>
import ButtonPrimary from '@/components/Button/ButtonPrimary.vue'
import { useStockStore } from '../stores/stock.store'
const store = useStockStore()
</script>

<template>
  <div>
    <p class="pb-3">Stock Management With Pinia</p>
    <table class="w-full table-auto">
      <!-- table Head -->
      <tr class="bg-gray-300">
        <td class="px-5 py-2 border-gray-500 border font-semibold">NAME</td>
        <td class="px-5 py-2 border-gray-500 border font-semibold">QUANTITY</td>
        <td class="px-5 py-2 border-gray-500 border font-semibold">ACTION</td>
      </tr>
      <!-- table Data -->
      <tr class="bg-gray-200" v-for="(stock, index) in store.stock_list" :key="index">
        <td class="px-5 py-2 border-gray-500 border">{{ stock.name }}</td>
        <td class="px-5 py-2 border-gray-500 border">{{ stock.qty }}</td>
        <td class="px-5 py-2 border-gray-500 border">
          <ButtonPrimary @click="store.decreaseStock(index)" class="mr-2"> - </ButtonPrimary>
          <ButtonPrimary @click="store.increaseStock(index)"> + </ButtonPrimary>
        </td>
      </tr>
    </table>
  </div>
</template>
