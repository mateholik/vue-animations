<template>
  <div id="app">
    <section>
      <div class="container">
        <div class="content">
          <button @click="exampleOneShow = !exampleOneShow">toggle</button>
          <Transition name="fade">
            <h1 v-show="exampleOneShow">Example 1</h1>
          </Transition>
        </div>
      </div>
    </section>

    <section>
      <div class="container">
        <div class="content">
          <button @click="exampleTwoShow = !exampleTwoShow">toggle</button>
          <Transition name="slide-fade">
            <h1 v-show="exampleTwoShow">Example 2</h1>
          </Transition>
        </div>
      </div>
    </section>

    <section>
      <div class="container">
        <div class="content">
          <button @click="exampleThreeShow = !exampleThreeShow">toggle</button>
          <Transition name="bounce">
            <h1 v-show="exampleThreeShow">Example 3</h1>
          </Transition>
        </div>
      </div>
    </section>

    <section>
      <div class="container">
        <div class="content">
          <button @click="exampleFourShow = !exampleFourShow">toggle</button>
          <Transition
            enter-active-class="animated tada"
            leave-active-class="animated bounceOutRight"
          >
            <h1 v-show="exampleFourShow">Example 4</h1>
          </Transition>
        </div>
      </div>
    </section>

    <section>
      <div class="container">
        <div class="content">
          <button @click="exampleFiveShow = !exampleFiveShow">toggle</button>
          <br />
          <Transition name="fade" mode="out-in">
            <button v-if="exampleFiveShow" key="save">Save</button>
            <button v-else key="edit">Edit</button>
          </Transition>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      exampleOneShow: false,
      exampleTwoShow: false,
      exampleThreeShow: false,
      exampleFourShow: false,
      exampleFiveShow: false,
    };
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
  @apply bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mb-8 transition duration-200;
}
h1 {
  @apply text-3xl uppercase bg-green-600 p-2 text-center;
  font-family: "Oswald", sans-serif;
}
/**/
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
/**/
.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(10px);
  opacity: 0;
}
/**/
.bounce-enter-active {
  animation: bounce-in 4s;
}
.bounce-leave-active {
  animation: bounce-in 4s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
/**/
</style>
