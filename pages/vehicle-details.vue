<template>
  <div class="px-4 py-8 sm:px-0 max-w-xl">
    <!-- <div class="p-12 rounded-lg border-4 border-dashed border-gray-200"> -->
      <div class="py-4">
        <Cards></Cards> 
      </div>
      <div class="mt-4 text-base font-medium text-gray-900">Vehicle Details</div>
      <div class="py-4">
        <MakeModel></MakeModel>
      </div>
      <div class="mt-4 text-base font-medium text-gray-900">Vehicle Color</div>
      <div class="py-4">
        <ColorPicker></ColorPicker>
      </div>
    <!-- </div> -->
  </div>
</template>

<script setup>
  //Set the route meta so it can be referenced in navbar
 definePageMeta({
   title: "Vehicle",
   order: 4
 })

 const route = useRoute();

 // Set the Page Title
 useHead({
   title:  route.meta.order + '. ' + route.meta.title
 })
</script>