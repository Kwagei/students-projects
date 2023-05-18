<template>
 <div class="mx-auto max-w-7xl pb-4 lg:px-8">
        <div as="div" v-for="cohort, i in cohorts" :key="i" class="pb-6">
                      
              <div class="flex w-full items-start justify-between text-left text-gray-200 text-xl bg-gray-500 p-6 cursor-pointer" @click="togglePanel(i)">                
                <span class="text-base font-semibold leading-7">{{ cohort.title}}</span>

                <span class="ml-6 flex h-7 items-center">
                  <PlusSmallIcon  v-if="!cohort.option" class="h-6 w-6" aria-hidden="true" />
                   
                  <MinusSmallIcon v-else class="h-6 w-6" aria-hidden="true" />
                </span>
              </div> 

              <div as="dd" class="mt-2 pr-12">
                <div class="text-base leading-7 text-gray-200" v-if="cohort.option">
                  <ul role="list" class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-3">
                  <li v-for="content, i in cohort.contents" :key="i" class="col-span-1 divide-y divide-gray-200 rounded-lg bg-white shadow">
                    <div class="flex w-full items-center justify-between space-x-6 p-6">
                      <div class="flex-1 truncate">
                        <div class="flex items-center space-x-3">
                          <h3 class="truncate text-sm font-medium text-gray-900">{{ content.name }}</h3>
                          <span class="inline-flex flex-shrink-0 items-center rounded-full bg-green-50 px-1.5 py-0.5 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">{{ content.role }}</span>
                        </div>
                        <p class="mt-1 truncate text-sm text-gray-500">{{ content.title }}</p>
                      </div>
                      <img class="h-10 w-10 flex-shrink-0 rounded-full bg-gray-300" :src="content.imageUrl" alt="" />
                    </div>
                    <div>
                      <div class="-mt-px flex divide-x divide-gray-200">
                        <div class="flex w-0 flex-1">
                          <a :href="`mailto:${content.email}`" class="relative -mr-px inline-flex w-0 flex-1 items-center justify-center gap-x-3 rounded-bl-lg border border-transparent py-4 text-sm font-semibold text-gray-900">
                            <EnvelopeIcon class="h-5 w-5 text-gray-400" aria-hidden="true" />
                            Email
                          </a>
                        </div>
                        <div class="-ml-px flex w-0 flex-1">
                          <a :href="`tel:${content.telephone}`" class="relative inline-flex w-0 flex-1 items-center justify-center gap-x-3 rounded-br-lg border border-transparent py-4 text-sm font-semibold text-gray-900">
                            <PhoneIcon class="h-5 w-5 text-gray-400" aria-hidden="true" />
                            Call
                          </a>
                        </div>
                      </div>
                    </div>
                  </li>
                </ul>
                </div>
              </div>
              
            </div> 
      </div>  
</template>

<script setup>
import { EnvelopeIcon, PhoneIcon } from '@heroicons/vue/20/solid'

import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { MinusSmallIcon, PlusSmallIcon } from '@heroicons/vue/24/outline'
import { computed, ref } from 'vue'

const cohorts = ref([
{
    title: "COHORT I",
    contents:
    [
  {
    name: 'Albin N. Karmo',
    title: 'Emerging Software Engineer',
    role: 'Developer',
    email: 'albin@kwagei.com',
    telephone: '+231-770-770-770',
    imageUrl:
      '/img/albin-n-karmo.jpeg',
  },
  {
    name: 'James K. Gaye, Jr.',
    title: 'Emerging Software Engineer',
    role: 'Developer',
    email: 'james@kwagei.com',
    telephone: '+231-770-770-770',
    imageUrl:
      '/img/james-k-gaye.jpg',
  },
  {
    name: 'Boakai Dubor Kamara',
    title: 'Emerging Software Engineer',
    role: 'Developer',
    email: 'boakaidorborkamara@gmail.com',
    telephone: '+231-770-770-770',
    imageUrl:
      '/img/boakai-d-kamara.jpeg',
  },
  {
    name: 'Benjamin A. Ngafua',
    title: 'Emerging Software Engineer',
    role: 'Developer',
    email: 'benjamin@kwagei.com',
    telephone: '+231-775-939-247',
    imageUrl:
      '/img/ben.jpeg',
  },
  {
    name: 'Joseph Gbakutu',
    title: 'Emerging Software Engineer',
    role: 'Developer',
    email: 'josephgbakutu@gmail.com',
    telephone: '+231-770-770-770',
    imageUrl:
      '/img/joseph-gbakutu.jpg',
  }
],
      option: false
  },
{
    title: "COHORT II",
    answer:
      "I don't know, but the flag is a big plus.",
      option: false
  }
])
const togglePanel = (index)=>{

    cohorts.value.forEach((element, i) => {
      
        element.option =(i==index)? !element.option : false
      
    });
}
</script>