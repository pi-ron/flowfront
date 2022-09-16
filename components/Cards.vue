<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <RadioGroup v-model="selectedMailingLists">
    <RadioGroupLabel class="text-base font-medium text-gray-900">Vehicle Size</RadioGroupLabel>

    <div class="mt-4 grid grid-cols-1 gap-y-6 sm:grid-cols-4 sm:gap-x-4">
      <RadioGroupOption as="template" v-for="mailingList in mailingLists" :key="mailingList.id" :value="mailingList" v-slot="{ checked, active }">
        <div :class="[checked ? 'border-transparent' : 'border-gray-300', active ? 'border-indigo-500 ring-2 ring-indigo-500' : '', 'relative flex cursor-pointer rounded-lg border bg-white p-4 shadow-sm focus:outline-none']">
          <span class="flex flex-1">
            <span class="flex flex-col">
              <RadioGroupLabel as="span" class="block text-sm font-medium text-gray-900">{{ mailingList.title }}</RadioGroupLabel>
              <RadioGroupDescription as="span" class="mt-1 flex items-center text-sm text-gray-500">{{ mailingList.description }}</RadioGroupDescription>
            </span>
          </span>
          <CheckCircleIcon :class="[!checked ? 'invisible' : '', 'h-5 w-5 text-indigo-600']" aria-hidden="true" />
          <span :class="[active ? 'border' : 'border-2', checked ? 'border-indigo-500' : 'border-transparent', 'pointer-events-none absolute -inset-px rounded-lg']" aria-hidden="true" />
        </div>
      </RadioGroupOption>
    </div>
  </RadioGroup>
</template>

<script setup>
import { ref } from 'vue'
import { RadioGroup, RadioGroupDescription, RadioGroupLabel, RadioGroupOption } from '@headlessui/vue'
import { CheckCircleIcon } from '@heroicons/vue/20/solid/index.js'

const mailingLists = [
  { id: 1, title: 'Small', description: 'Hatch backs and scooters', users: '$99' },
  { id: 2, title: 'Medium', description: 'Horse and Goats', users: '$199' },
  { id: 3, title: 'Large', description: 'Camels, Giraffes etc.', users: '$299' },
  { id: 4, title: 'Oversize', description: 'Elephants, whales etc.', users: '$299' },
]

const selectedMailingLists = ref(mailingLists[0])
</script>