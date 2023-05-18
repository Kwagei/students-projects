<template>
  <div>
    <!-- Header -->
    <div class="relative pb-32 bg-no-repeat bg-cover bg-fixed bg-[linear-gradient(to_right_bottom,rgba(2,3,1,0.7),rgba(6,21,82,0.7)),url(/img/bg1.jpg)]">
      <!-- <div class="absolute inset-0">
        <img class="h-full w-full object-cover" src="https://images.unsplash.com/photo-1525130413817-d45c1d127c42?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1920&q=60&&sat=-100" alt="" />
        <div class="absolute inset-0 bg-gray-800 mix-blend-multiply" aria-hidden="true" />url(https://images.unsplash.com/photo-1525130413817-d45c1d127c42?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1920&q=60&&sat=-100)
      </div> -->
      <div class="relative mx-auto max-w-7xl px-6 py-24 sm:py-32 lg:px-8">
        <h1 class="text-4xl font-bold tracking-tight text-white md:text-5xl lg:text-5xl leading-loose">We are mastery innovators!</h1>
        <p class="mt-6 max-w-3xl text-2xl text-gray-300 leading-loose">Our style of learning is <b>mastery-based</b>; 
           on top of atomic concepts, <br/>
           we chain our learning. We are ready to <code>code</code> your dream <br/> 
           into a reality!!</p>
      
          <button type="button" class="mt-6 text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
            Join Us Now!
            <svg aria-hidden="true" class="w-5 h-5 ml-2 -mr-1" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
        </button>
      </div>
    </div>

    <!-- Overlapping cards -->
    <section class="relative z-10 mx-auto -mt-32 max-w-5xl px-6 pb-16 lg:px-8" aria-labelledby="contact-heading">
      <h2 class="sr-only" id="contact-heading">Contact us</h2>
      <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-3">
        <div v-for="link in supportLinks" :key="link.name" class="flex flex-col items-stretch rounded-2xl bg-white shadow-xl bg-gray-200">
          <div class="relative flex-1 px-0 md:px-0">
            <!-- <div class="absolute top-0 inline-block -translate-y-1/2 transform rounded-xl bg-indigo-600 p-5 shadow-lg">
              <component :is="link.icon" class="h-6 w-6 text-white" aria-hidden="true" />
            </div> -->
              <div class="grid place-items-center relative h-60 w-full overflow-hidden rounded-lg"><img class="w-full flex-shrink-0" :src="link.img" alt="" /> 
              </div>
              <div class="my-2">
                <h3 class="text-l font-medium text-gray-900 self-center text-center">{{ link.name }}</h3>
              </div>
          </div>
          <div class="rounded-bl-2xl rounded-br-2xl bg-gray-50 p-6 md:px-8 text-center">
            <a :href="link.href" class="text-base font-medium text-indigo-700 hover:text-indigo-600">View project<span aria-hidden="true"> &rarr;</span></a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { LifebuoyIcon, NewspaperIcon, PhoneIcon } from '@heroicons/vue/24/outline'

const supportLinks = [
  {
    name: 'Census 2008',
    href: 'https://benjaminangafua.github.io/liberia-census2008/index.html',
    img:'/img/census-2008.png',    
    icon: PhoneIcon,
  },
  {
    name: 'Tic-Tac-Toe Game',
    href: 'https://kwagei.github.io/week-six-assignment-kanmuteh1/tic-tac-toe/index.html',
    img:
    '/img/tic-tac-toe.png',
      icon: LifebuoyIcon,
  },
  {
    name: 'Tic-Tac-Toe Game',
    href: 'https://kwagei.github.io/week-five-assignment-boakaidorborkamara/',
    img:
    '/img/guess-game.png',
      icon: LifebuoyIcon,
  },
]
</script>