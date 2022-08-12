<template>
  <div id="app">
    <Example1 />
    <Example2 />
    <Example3 />
    <Example4 />
    <Example5 />
    <Example6 />
    <Example7 />
    <Example8 />
    <Example9 />
    <Example10 />
  </div>
</template>

<script>
import Example1 from "./components/Example1.vue";
import Example2 from "./components/Example2.vue";
import Example3 from "./components/Example3.vue";
import Example4 from "./components/Example4.vue";
import Example5 from "./components/Example5.vue";
import Example6 from "./components/Example6.vue";
import Example7 from "./components/Example7.vue";
import Example8 from "./components/Example8.vue";
import Example9 from "./components/Example9.vue";
import Example10 from "./components/Example10.vue";
export default {
  components: {
    Example1,
    Example2,
    Example3,
    Example4,
    Example5,
    Example6,
    Example7,
    Example8,
    Example9,
    Example10,
  },
};
</script>

<style lang="postcss">
section {
  @apply p-5 h-screen;
}
section:nth-child(odd) {
  @apply bg-blue-100;
}
section:nth-child(even) {
  @apply bg-red-100;
}
.container {
  @apply max-w-7xl h-full mx-auto rounded-md border-2 border-solid border-gray-300 p-5 flex justify-center;
}
.content {
  @apply max-w-2xl w-full mx-auto;
}
button {
  @apply bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mb-8 transition duration-200 mr-4;
}
h1 {
  @apply text-3xl uppercase bg-green-600 p-2 text-center text-white;
  font-family: "Oswald", sans-serif;
}
</style>
