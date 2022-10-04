<script setup lang="ts"></script>

<template>
  <div class="version">
    <img
      src="https://img.icons8.com/ios-filled/100/000000/paint.png"
      alt="brush icon"
    />
    <a class="vlink" href="https://ahmed.systems"> A </a>
    <a class="vlink" href="https://b.ahmed.systems"> B </a>
    <a class="vlink" href="https://c.ahmed.systems"> C </a>
    <a class="vlink" href="https://d.ahmed.systems"> D </a>
    <a class="selected" href="https://e.ahmed.systems"> E </a>
  </div>
</template>

<style scoped>
  .version,
  .version * {
    font-family: sans-serif;
  }
  .version {
    position: fixed;
    bottom: 1rem;
    right: 1rem;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    background-color: #222;
    color: whitesmoke;
    box-shadow: 0px 0px 8px gray;
    border-radius: 1rem;
    padding: 0.2rem 0.5rem;
  }
  .version > .vlink,
  .version > .selected {
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    border-radius: 50%;
    padding: 0.1rem 0.5rem;
  }
  .version > .selected {
    background-color: darkseagreen;
    cursor: default;
    color: #222;
  }
  .version > .vlink:hover {
    background-color: darkgray;
    color: #222;
  }
  .version > img {
    padding: 0.3rem;
    width: 2rem;
    filter: invert(1);
    opacity: 0.8;
  }
</style>
