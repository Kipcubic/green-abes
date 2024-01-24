<template>
      <main class="mx-auto  max-w-7xl px-4 px-6 sm:mt-12 lg:mt-16">
    <div class="lg:grid lg:grid-cols-12 lg:gap-8">
      <div class="sm:text-center md:mx-auto md:max-w-2xl lg:col-span-6 lg:text-left">
        <h1>
          <span class="block text-base font-semibold text-gray-500 sm:text-lg lg:text-base xl:text-lg">Green Abes</span>
          <span class="mt-1 block text-2xl font-bold tracking-tight sm:text-4xl xl:text-6xl">
            <span class="block text-gray-900">Empower. Gift. Grow.</span>
            <span class="block text-green-600">Join the Movement</span>
          </span>
        </h1>
        <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl">
          Join us, where your support transforms lives. Gift joy, plant trees, build communities. Together, we create sustainable change and make a lasting impact. Donate now.
        </p>
        <div class="mt-8 sm:mx-auto sm:max-w-lg sm:text-center lg:mx-0 lg:text-left">
          <!-- <p class="text-base font-medium text-gray-900">Donate Now.</p> -->
          <div class="mt-10 flex items-center gap-x-6">
      <a href="#" class="rounded-md bg-green-500 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-green-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-dark-400">Donate Now</a>
      <a href="#" class="text-sm font-semibold leading-6 text-dark">Sign Up <span aria-hidden="true">→</span></a>
    </div>
          <p class="mt-3 text-sm text-gray-500">
            We care about the protection of your data. Read our
            <a href="#" class="font-medium text-gray-900 underline">Privacy Policy</a>.
          </p>
        </div>
      </div>
      <div class="relative mt-12 sm:mx-auto sm:max-w-lg lg:col-span-6 lg:mx-0 lg:mt-0 lg:flex lg:max-w-none lg:items-center">
        <svg class="absolute left-1/2 top-0 origin-top -translate-x-1/2 -translate-y-8 scale-75 transform sm:scale-100 lg:hidden" width="640" height="784" fill="none" viewBox="0 0 640 784" aria-hidden="true">
          <defs>
            <pattern id="4f4f415c-a0e9-44c2-9601-6ded5a34a13e" x="118" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect y="72" width="640" height="640" class="text-gray-50" fill="currentColor" />
          <rect x="118" width="404" height="784" fill="url(#4f4f415c-a0e9-44c2-9601-6ded5a34a13e)" />
        </svg>
        <div class="relative mx-auto w-full rounded-lg shadow-lg ">
            <img class="w-full" src="/banner-new.jpg" alt="" />
          
        </div>
      </div>
    </div>
  </main>
</template>
<script setup>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [
  { name: 'Home', href: '/' },
  { name: 'About us', href: '#' },
  { name: 'Gallery', href: '#' },
]
</script>