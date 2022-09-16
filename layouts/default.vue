<template>
  <div class="min-h-full">
    <Navbar />
    <div class="py-10">
      <header>
        <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
          <h1 class="text-3xl font-bold leading-tight tracking-tight text-gray-900">{{ route.meta.title }}</h1>
        </div>
      </header>  
      <main>
        <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
          <slot />
          <Progress></Progress>
          
        </div>
      </main>
    </div>
  </div>
</template>

<script setup>
  const route = useRoute(); // this gives us access to route.meta where the title is defined
</script>