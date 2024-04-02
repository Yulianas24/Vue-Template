<script setup>
import SectionNavbar from '../components/Section/SectionNavbar.vue'
import SectionMain from '../components/Section/SectionMain.vue'
import SectionFooter from '../components/Section/SectionFooter.vue'
</script>

<template>
  <div class="flex flex-col gap-5 w-screen h-screen">
    <!-- navbar -->
    <SectionNavbar />
    <!-- main content -->
    <SectionMain>
      <p>Main Section</p>
    </SectionMain>
    <!-- footer -->
    <SectionFooter />
  </div>
</template>
