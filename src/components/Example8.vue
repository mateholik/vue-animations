<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="exampleEightShow = !exampleEightShow">
          toggle example 8
        </button>
        <div class="max-w-md">
          <div class="border-4 border-solid border-green-300 p-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque
            neque quaerat labore, deleniti totam odit possimus facere voluptate
            nam voluptatum.
          </div>

          <transition name="collapse">
            <div
              v-if="exampleEightShow"
              class="max-h-96 h-auto overflow-hidden"
            >
              <p class="p-4 border-4 border-solid border-red-300">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Maiores blanditiis quo doloribus consequuntur quae iure pariatur
                modi aperiam, cupiditate porro. Inventore asperiores accusamus
                tempora necessitatibus sint dolores deleniti eum. Molestias,
                ipsa repellendus explicabo soluta quos odio sapiente adipisci
                qui. Animi.
              </p>
            </div>
          </transition>

          <div class="border-4 border-solid border-blue-300 p-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero,
            non!
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      exampleEightShow: true,
    };
  },
};
</script>

<style>
.collapse-enter,
.collapse-leave-to {
  max-height: 0;
}
.collapse-enter-active,
.collapse-leave-active {
  transition: 1s;
}
</style>
