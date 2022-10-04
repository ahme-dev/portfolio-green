<script setup lang="ts">
  import Card from "./Card.vue";
</script>

<template>
  <div
    id="container"
    class="min-w-screen min-h-screen bg-gray-200 snap-y snap-mandatory overflow-y-scroll"
  >
    <!-- Header -->
    <header
      id="header"
      class="flex flex-col items-center justify-center gap-8 p-8 min-h-screen md:( w-1/2 m-auto) snap-center"
    >
      <h1 class="p-4 text-4xl font-bold text-gray-800">My name's Ahmed</h1>
      <Card>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo sit
        perspiciatis reprehenderit nam perferendis ut obcaecati inventore, quia
        sed velit rerum possimus, expedita molestiae doloribus dolor delectus
        harum quasi fugit.
      </Card>
    </header>
    <!-- Header End -->

    <!-- Main -->
    <main
      class="flex flex-col justify-center items-center p-8 gap-8 min-h-screen md:(w-1/2 m-auto) snap-center"
    >
      <h1 class="p-4 text-2xl font-bold self-start">Projects</h1>
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
  </div>
</template>
