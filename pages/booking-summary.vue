<template>
  <div class="px-4 py-8 sm:px-0">
    <div class="h-96 rounded-lg border-4 border-dashed border-gray-200">
      Booking Summary
    </div>
  </div>
</template>

<script setup>
  //Set the route meta so it can be referenced in navbar
 definePageMeta({
   title: "Booking Summary",
   order: 8
 })

 const route = useRoute();

 // Set the Page Title
 useHead({
   title:  route.meta.order + '. ' + route.meta.title
 })
</script>