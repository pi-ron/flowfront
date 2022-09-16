<!--
  This example requires Tailwind CSS v2.0+ 
  
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->
<template>
  <div class="isolate -space-y-px rounded-md shadow-sm">
    <div class="relative rounded-md rounded-b-none border border-gray-300 px-3 py-2 focus-within:z-10 focus-within:border-indigo-600 focus-within:ring-1 focus-within:ring-indigo-600">
      <label for="Year" class="block text-xs font-medium text-gray-900">Year</label>
      <input type="text" name="Year" id="Year" class="block w-full border-0 p-0 text-gray-900 placeholder-gray-500 focus:ring-0 sm:text-sm" placeholder="e.g. 2014" />
    </div>
    <div class="relative border border-gray-300 px-3 py-2 focus-within:z-10 focus-within:border-indigo-600 focus-within:ring-1 focus-within:ring-indigo-600">
      <label for="Make" class="block text-xs font-medium text-gray-900">Make</label>
      <input type="text" name="make" id="make" class="block w-full border-0 p-0 text-gray-900 placeholder-gray-500 focus:ring-0 sm:text-sm" placeholder="e.g. Toyota" />
    </div>
    <div class="relative rounded-md rounded-t-none border border-gray-300 px-3 py-2 focus-within:z-10 focus-within:border-indigo-600 focus-within:ring-1 focus-within:ring-indigo-600">
      <label for="model" class="block text-xs font-medium text-gray-900">Model</label>
      <input type="text" name="model" id="model" class="block w-full border-0 p-0 text-gray-900 placeholder-gray-500 focus:ring-0 sm:text-sm" placeholder="e.g. Yaris" />
    </div>
  </div>
</template>
