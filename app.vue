<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
  
  // console.log(useRouter().getRoutes());
useHead({
  title: "Testing thing",
  // or, instead:
  // titleTemplate: (title) => `My App - ${title}`,
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1',
  charset: 'utf-8',
  meta: [
    { name: 'description', content: 'HappyDetailerX Quiz Flow.' }
  ],
  bodyAttrs: {
    class: 'h-full'
  },
  htmlAttrs: {
    class: 'h-full'
  }
})

// const { data: companyRemote } = await useFetch(() => `https://xpt5-jmyh-njch.n7.xano.io/api:ilDhAZ8n/company`, { params: { siteUrl: 
//   'https://devdisaster.happydetailer.com' } })
</script>