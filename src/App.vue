<script setup lang="ts">
  import Card from "./Card.vue";
</script>

<template>
  <div
    id="container"
    class="min-w-screen min-h-screen text-gray-800 bg-gray-200 snap-y snap-mandatory overflow-y-scroll"
  >
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
          href="#projects"
          class="bg-emerald-300 p-4 font-bold text-gray-800 hover:(shadow-lg shadow-emerald-300)"
          >Projects</a
        >

        <a
          href="#skills"
          class="bg-emerald-300 p-4 font-bold text-gray-800 hover:(shadow-lg shadow-emerald-300)"
          >Skills</a
        >

        <a
          href="#contact"
          class="bg-emerald-300 p-4 font-bold text-gray-800 hover:(shadow-lg shadow-emerald-300)"
          >Contact</a
        >
      </nav>
    </header>
    <!-- Header End -->

    <!-- Main -->
    <main
      class="flex flex-col justify-center items-center p-8 gap-8 min-h-screen md:(w-1/2 m-auto) snap-center"
    >
      <h1
        id="projects"
        class="mt-24 p-4 text-2xl font-bold self-start text-gray-800 bg-emerald-300 hover:(shadow-lg shadow-emerald-300)"
      >
        Projects
      </h1>
      <Card>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus at
        aperiam modi, itaque reiciendis asperiores nemo ipsa consequatur sed
        doloribus, maiores veritatis laudantium assumenda, eaque ut recusandae.
        Asperiores consequatur beatae voluptate quia ipsam error nulla ducimus
        vel et perspiciatis rerum praesentium, quod tempore, ratione iusto sit
        esse cupiditate doloremque laborum.
      </Card>
      <Card>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. A quis quas
        illo perferendis nesciunt commodi reiciendis maxime recusandae cum iure
        sunt, asperiores ab aut?
      </Card>

      <h1
        id="skills"
        class="mt-24 p-4 text-2xl font-bold self-start text-gray-800 bg-emerald-300 hover:(shadow-lg shadow-emerald-300)"
      >
        Skills
      </h1>
      <Card>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus at
        aperiam modi, itaque reiciendis asperiores nemo ipsa consequatur sed
        doloribus, maiores veritatis laudantium assumenda, eaque ut recusandae.
        Asperiores consequatur beatae voluptate quia ipsam error nulla ducimus
        vel et perspiciatis rerum praesentium, quod tempore, ratione iusto sit
        esse cupiditate doloremque laborum.
      </Card>
      <Card>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. A quis quas
        illo perferendis nesciunt commodi reiciendis maxime recusandae cum iure
        sunt, asperiores ab aut?
      </Card>
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
  </div>
</template>
