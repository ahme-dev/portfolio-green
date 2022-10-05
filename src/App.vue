<script setup lang="ts">
  import Card from "./Card.vue";
  import Version from "./Version.vue";
  import { info } from "./info";
</script>

<template>
  <div
    id="container"
    class="min-w-screen min-h-screen text-gray-800 bg-gray-200 snap-y snap-mandatory overflow-y-scroll"
  >
    <img
      class="fixed filter blur-3xl min-h-screen w-screen z-0 opacity-20"
      src="./assets/layered-steps-haikei.svg"
    />
    <!-- Header -->
    <header
      id="header"
      class="flex flex-col items-center justify-center gap-8 p-8 min-h-screen md:( w-1/2 m-auto) snap-center"
    >
      <h1 class="p-4 text-4xl font-bold text-gray-800">
        My name's <span class="bg-emerald-300 px-2">Ahmed</span>
      </h1>
      <Card>
        At this point, I can't write more nonesense, so we'll go with Lorem,
        ipsum dolor sit amet consectetur adipisicing elit. Quisquam doloremque
        corporis voluptatibus, harum fuga tempora voluptate laborum quod
        dignissimos rem. Recusandae repellendus quo facilis? Molestiae nobis
        tempora autem officia reprehenderit.
      </Card>
      <nav class="flex gap-4 m-4">
        <a
          v-for="el in info"
          :href="'#' + el.title.toLowerCase()"
          class="bg-emerald-300 p-4 font-bold text-gray-800 hover:(shadow-lg shadow-emerald-300)"
          >{{ el.title }}</a
        >
      </nav>
    </header>
    <!-- Header End -->

    <!-- Main -->
    <main
      class="flex flex-col justify-center items-center p-8 gap-8 min-h-screen"
    >
      <div
        class="flex flex-col justify-center items-start p-8 gap-8 md:(w-1/2 m-auto)"
        v-for="el in info"
      >
        <h1
          :id="el.title.toLowerCase()"
          class="mt-24 p-4 text-2xl font-bold self-start text-gray-800 bg-emerald-300 hover:(shadow-lg shadow-emerald-300)"
        >
          {{ el.title }}
        </h1>
        <Card v-for="item in el.items"> {{ item }} </Card>
      </div>
    </main>
    <!-- Main End -->
    <!-- Footer Start -->
    <footer
      id="contact"
      class="flex items-center justify-center gap-4 bg-emerald-300 mt-24"
    >
      <a
        href="https://github.com/ahmedkabd/e.ahmed.systems"
        class="p-4 text-lg text-gray-800 hover:(cursor-pointer bg-gray-200)"
        >Github</a
      >
      <a
        href="mailto:ahmadkabdullah@pm.me"
        class="p-4 text-lg text-gray-800 hover:(cursor-pointer bg-gray-200)"
        >Email</a
      >
      <a
        href="https://t.me/ahmedkabd"
        class="p-4 text-lg text-gray-800 hover:(cursor-pointer bg-gray-200)"
        >Telegram</a
      >
    </footer>
    <!-- Footer End -->
    <!-- Version Switcher -->
    <Version></Version>
    <!-- Fixed Symbols -->
    <a
      href="#header"
      class="fixed opacity-0 select-none md:(top-2 right-5 text-5xl text-gray-500 opacity-20) hover:(text-emerald-300 opacity-90)"
    >
      ◥
    </a>
  </div>
</template>
