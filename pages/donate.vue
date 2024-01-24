<template>
    <div class="bg-green-100/2 py-24 sm:py-16">
      <div class="relative isolate">
        <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
          <div class="mx-auto flex max-w-2xl flex-col gap-16 bg-white/5 px-6 py-16 ring-1 ring-white/10 sm:rounded-3xl sm:p-8 lg:mx-0 lg:max-w-none lg:flex-row lg:items-center lg:py-20 xl:gap-x-20 xl:px-20">
            <img class="h-96 w-full flex-none rounded-2xl object-cover shadow-xl lg:aspect-square lg:h-auto lg:max-w-sm" src="/donate.jpg" alt="Donate now" />
            <div class="w-full flex-auto">
              <h2 class="text-3xl font-bold tracking-tight text-dark sm:text-4xl">When you donate we achieve the following</h2>
              <!-- <p class="mt-6 text-lg leading-8 text-dark">Lorem ipsum dolor sit amet consect adipisicing elit. Possimus magnam voluptatum cupiditate veritatis in accusamus quisquam.</p> -->
              <ul role="list" class="mt-10 grid grid-cols-1 gap-x-8 gap-y-3 text-base leading-7 text-green-600 sm:grid-cols-2">
                <li v-for="benefit in benefits" :key="benefit" class="flex gap-x-3">
                  <CheckCircleIcon class="h-7 w-5 flex-none" aria-hidden="true" />
                  {{ benefit }}
                </li>
              </ul>
              <div class="mt-10 flex">

                <a href="">
                    Paypal
                </a>

              </div>
            </div>
          </div>
        </div>
        <div class="absolute inset-x-0 -top-16 -z-10 flex transform-gpu justify-center overflow-hidden blur-3xl" aria-hidden="true">
          <div class="aspect-[1318/752] w-[82.375rem] flex-none bg-gradient-to-r from-[#80caff] to-[#4f46e5] opacity-25" style="clip-path: polygon(73.6% 51.7%, 91.7% 11.8%, 100% 46.4%, 97.4% 82.2%, 92.5% 84.9%, 75.7% 64%, 55.3% 47.5%, 46.5% 49.4%, 45% 62.9%, 50.3% 87.2%, 21.3% 64.1%, 0.1% 100%, 5.4% 51.1%, 21.4% 63.9%, 58.9% 0.2%, 73.6% 51.7%)" />
        </div>
      </div>
    </div>
  </template>
   <!-- <script src="https://www.paypalobjects.com/donate/sdk/donate-sdk.js" charset="UTF-8"></script> -->

  <script setup>
  import { CheckCircleIcon } from '@heroicons/vue/20/solid'
  
  const benefits = [
    'Transform Lives',
    'Sustainable Impact',
    'Community Building',
    'Holistic Well-being',
    'Holistic Well-being',
    'Partnerships for Amplified Impact',
  ]
 
  </script>