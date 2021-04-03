<template>
  <Header />
  <section class="flex flex-col justify-center px-6 mx-auto max-w-7xl">
    <figure class="flex justify-center w-auto h-full">
      <img
        alt="Vue logo"
        src="./assets/logo.png"
      />
    </figure>
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
  </section>
  <div class="fixed z-30 flex justify-center w-full p-3 bottom-5">
    <p class="flex items-center w-auto px-4 py-1 mx-auto bg-white rounded-full shadow-xl">
      <span
        role="img"
        class="mr-2"
        style="font-size: 24px"
      >👻</span>
      <span>
        By browsing this website, you consent to our
        <a
          href="#"
          class="font-bold text-black"
        >Privacy Policy</a>
        <span class="mx-1">⏤</span>
        <span class="font-semibold text-indigo-500 ">I agree</span>
      </span>
    </p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";

export default defineComponent({
  name: "App",
  components: {
    HelloWorld,
    Header,
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
