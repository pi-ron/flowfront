<template>
    <div as="nav" class="border-b border-gray-200 bg-white">
      <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
        <div class="flex h-16 justify-between">
          <div class="flex">
            <div class="flex flex-shrink-0 items-center">
              <img class="block h-8 w-auto lg:hidden" :src="brand.fullLogoUrl" :alt="brand.name" />
              <img class="hidden h-8 w-auto lg:block" :src="brand.fullLogoUrl" :alt="brand.name" />
              
            </div>
            <div class="hidden sm:-my-px sm:ml-6 sm:flex sm:space-x-8">
              <!-- <a v-for="item in navigation" :key="item.name" :href="item.href" :class="[item.current ? 'border-indigo-500 text-gray-900' : 'border-transparent text-gray-500 hover:border-gray-300 hover:text-gray-700', 'inline-flex items-center px-1 pt-1 border-b-2 text-sm font-medium']" :aria-current="item.current ? 'page' : undefined">{{ item.name }}</a> -->
              <NuxtLink v-for="item in routes" :key="item.name" :href="item.path" activeClass="border-indigo-500 text-indigo-800" class="text-gray-500 hover:border-gray-300 hover:text-gray-700 inline-flex items-center px-1 pt-1 border-b-2 text-sm font-medium" :aria-current="item.current ? 'page' : undefined">{{ item.meta.title }}</NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script setup>
  
  const user = {
    name: 'Chris Smartwax',
    email: 'chris@smartwaxam.com',
    imageUrl:
      'https://uploads-ssl.webflow.com/63115b3146c11a4ff413a88f/6311623c3157c4eb2fd6529a_Chris%20Lorizio%20Headshot.png',
  }

  // Get routes to use for navbar
  const routesRaw = useRouter().getRoutes();

  //Sort them by meta.order integer
  const routes = routesRaw.sort(function(a, b) {
    return parseFloat(a.meta.order) - parseFloat(b.meta.order);
  });
  
  // console.log(routes);

  const userNavigation = [
    { name: 'This', href: '#' },
    { name: 'Does', href: '#' },
    { name: 'Nothing', href: '#' },
  ]

  const brand = {
    name: "HappyDetailerX",
    fullLogoUrl: "https://uploads-ssl.webflow.com/63115b3146c11a4ff413a88f/6318ea0358aeed4a06d7539c_HappyDetailerLogoColor.png",
    iconLogoUrl: "https://uploads-ssl.webflow.com/63115b3146c11a4ff413a88f/6311623c3157c4eb2fd6529a_Chris%20Lorizio%20Headshot.png",
    ownerHeadshotUrl: "https://uploads-ssl.webflow.com/63115b3146c11a4ff413a88f/6311623c3157c4eb2fd6529a_Chris%20Lorizio%20Headshot.png"
  }
  </script>