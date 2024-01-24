<template>
  <div class="relative mx-auto max-w-7xl overflow-hidden bg-white">
<div class="hidden lg:absolute lg:inset-0 lg:block" aria-hidden="true">
  <svg class="absolute left-1/2 top-0 -translate-y-8 translate-x-64 transform" width="640" height="784" fill="none" viewBox="0 0 640 784">
    <defs>
      <pattern id="9ebea6f4-a1f5-4d96-8c4e-4c2abf658047" x="118" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
        <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
      </pattern>
    </defs>
    <rect y="72" width="640" height="640" class="text-gray-50" fill="currentColor" />
    <rect x="118" width="404" height="784" fill="url(#9ebea6f4-a1f5-4d96-8c4e-4c2abf658047)" />
  </svg>
</div>

<div class="relative pb-16 sm:pb-24 lg:pb-32">
  <Popover>
    <!-- <nav class="relative mx-auto flex max-w-7xl items-center justify-between px-6" aria-label="Global">
      <div class="flex flex-1 items-center">
        <div class="flex w-full items-center justify-between md:w-auto">
          <a href="#">
            <span class="sr-only">Green Abes</span>
            <img class="h-8 w-auto sm:h-10" src="/logo.svg" alt="logo" />
          </a>
          <div class="-mr-2 flex items-center md:hidden">
            <PopoverButton  class="relative inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-green-500">
              <span class="absolute -inset-0.5" />
              <span class="sr-only">Open main menu</span>
              <Bars3Icon class="h-6 w-6" aria-hidden="true" />
            </PopoverButton>
          </div>
        </div>
        <div class="hidden md:ml-10 md:block md:space-x-10">

          <NuxtLink v-for="item in navigation" :key="item.name" :to="item.href" class="font-medium text-gray-500 hover:text-gray-900">{{ item.name }}</NuxtLink>
        </div>
      </div>
      <div class="hidden text-right md:block">
        <span class="inline-flex rounded-md shadow-md ring-1 ring-black ring-opacity-5">
          <NuxtLink to="/donate" class="inline-flex items-center rounded-md border border-transparent bg-white px-4 py-2 text-base font-medium text-green-600 hover:bg-gray-50">Donate</NuxtLink>
        </span>
      </div>
    </nav> -->


    <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="/" class="-m-1.5 p-1.5">
            <span class="sr-only">Green Abes</span>
            <img class="h-24 w-auto" src="/logo.svg" alt="" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a v-for="item in navigation" :key="item.name" :href="item.href" class="text-sm font-semibold leading-6 text-gray-900">{{ item.name }}</a>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <a href="/donate" class="text-sm font-semibold leading-6 text-gray-900">Donate <span aria-hidden="true">&rarr;</span></a>
        </div>
      </nav>

      <!-- <PopoverPanel focus class="absolute inset-x-0 top-0 z-10 origin-top-right transform p-2 transition md:hidden">
        <div class="overflow-hidden rounded-lg bg-white shadow-md ring-1 ring-black ring-opacity-5">
          <div class="flex items-center justify-between px-5 pt-4">
            <div>
              <img class="h-8 w-auto" src="/logo.svg" alt="" />
            </div>
            <div class="-mr-2">
              <PopoverButton class="relative inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-green-500">
                <span class="absolute -inset-0.5" />
                <span class="sr-only">Close main menu</span>
                <XMarkIcon class="h-6 w-6" aria-hidden="true" />
              </PopoverButton>
            </div>
          </div>
          <div class="space-y-1 px-2 pb-3 pt-2">
            <a v-for="item in navigation" :key="item.name" :href="item.href" class="block rounded-md px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 hover:text-gray-900">{{ item.name }}</a>
          </div>
          <a href="#" class="block w-full bg-gray-50 px-5 py-3 text-center font-medium text-green-600 hover:bg-gray-100">Donate</a>
        </div>
      </PopoverPanel> -->
      <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <div class="fixed inset-0 z-50" />
        <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
          <div class="flex items-center justify-between">
            <a href="/" class="-m-1.5 p-1.5">
              <span class="sr-only">Your Company</span>
              <img class="h-12 w-auto" src="/logo.svg" alt="logo" />
            </a>
            <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a v-for="item in navigation" :key="item.name" :href="item.href" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">{{ item.name }}</a>
              </div>
              <div class="py-6">
                <a href="/donate" class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Donate</a>
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
  </Popover>

<NuxtPage/>
</div>
</div>
</template>
<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [
{ name: 'Home', href: '/' },
{ name: 'About us', href: '' },
{ name: 'Gallery', href: '' },
]

const mobileMenuOpen = ref(false)

useSeoMeta({
  title: 'Green Abes',
  ogTitle: 'Green Abes',
  description: 'Empowering communities through gifts and trees.',
  ogDescription: 'Empowering communities through gifts and trees.',
  ogImage: '/logo.svg',
  twitterCard: '/logo.svg',
})
</script>