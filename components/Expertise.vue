<template>
  <div class="mt-8">
    <div class="mt-2">
      <h2 class="mb-2 text-xl text-gray-700 font-bold dark:text-blue-200 capitalize">
        Frontend
      </h2>

      <ul class="flex flex-wrap gap-4 items-center">

        <!--  <li class="flex items-center">
          <svg class="h-10 w-10" xmlns="http://www.w3.org/2000/svg">
            <image href="../assets/devicon/angular.svg" height="40" width="40" />

          </svg>
        </li> -->
        <!--    <li class="flex items-center">
          <Angular class="h-10 w-10"></Angular>
        </li>
        <li class="flex items-center">
          <Bootstrap class="h-10 w-10"></Bootstrap>
        </li>
        <li class="flex items-center">
          <TailwindCss class="h-10 w-10"></TailwindCss>
        </li>
        <li class="flex items-center">
          <Javascript class="h-10 w-10"></Javascript>
        </li> -->
        <li class="flex items-center">
          <Vuejs class="h-10 w-10"></Vuejs>
        </li>

        <li class="flex items-center">
          <React class="h-10 w-10"></React>
        </li>
      </ul>
    </div>
    <div class="mt-4">
      <h2 class="mb-2 text-xl text-gray-700 font-bold dark:text-blue-200 capitalize">
        Backend
      </h2>
      <ul class="mb-6 flex flex-wrap gap-4">
        <li class="flex items-center">
          <Laravel class="h-10 w-10"></Laravel>
        </li>

        <!--     <li class="flex items-center"> -->
        <!-- <Symfony class="h-10 w-10"></Symfony> -->
        <!--     <svg class="h-10 w-10" xmlns="http://www.w3.org/2000/svg">
            <image href="../assets/devicon/nest.svg" height="40" width="40" />
          </svg>
        </li> -->
        <!-- <li class="flex items-center">
         
          <svg class="h-10 w-10" xmlns="http://www.w3.org/2000/svg">

            <image href="../assets/devicon/symfony.svg" height="40" width="45" />

          </svg>
        </li>
        <li class="flex items-center">
          <Next class="h-10 w-10"></Next>
        </li>
        <li class="flex items-center">
          <Nuxt class="h-10 w-10"></Nuxt>
        </li>
        <li class="flex items-center">
          <Node class="h-10 w-10"></Node>
        </li> -->
      </ul>
    </div>
  </div>
</template>

<script>

import Vuejs from "../assets/devicon/vuejs.svg?inline";
import TailwindCss from "../assets/devicon/tailwindcss.svg?inline";
import Nuxt from "../assets/devicon/nuxt.svg?inline";
import Bootstrap from "../assets/devicon/bootstrap.svg?inline";
import Laravel from "../assets/devicon/laravel.svg?inline";

import React from "../assets/devicon/react.svg?inline";

import Node from "../assets/devicon/node.svg?inline";

export default {
  components: {
    Bootstrap,
    Vuejs,
    TailwindCss,
    Nuxt,
    Laravel,
    Node,
    React,
  },
};
</script>
